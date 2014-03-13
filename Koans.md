### Koans - Symbols
##### case 72
심볼은 C언어에서의 상수처럼 생각하면 될것 같다. 아래 두번째 test에서 두 객체의 object_id는 동일하다.
```ruby
def test_identical_symbols_are_a_single_internal_object
    symbol1 = :a_symbol
    symbol2 = :a_symbol

    assert_equal true, symbol1           == symbol2
    assert_equal false, symbol1.object_id == symbol2.object_id
end
```
##### case 73
`Symbol.all_symbols`로 모든 심볼을 확인할수 있다. 화면 가득 채운 심볼들로 놀라게 될것이다. Ruby 내부적으로는 모든 참조되는 것들은 심볼로 관리하는 것이 아닌가 생각된다. 이 test는 함수 이름도 심볼로 등록된다는 것을 보여준다.

    def test_method_names_become_symbols
        symbols_as_strings = Symbol.all_symbols.map { |x| x.to_s }
        assert_equal __, symbols_as_strings.include?("test_method_names_become_symbols")
    end

    # THINK ABOUT IT:
    #
    # Why do we convert the list of symbols to strings and then compare
    # against the string value rather than against symbols?

##### case 74
`"What is the sound of one hand clapping?"`는 심볼로 저장되지 않고, constant 이름이 심볼로 저장된다.

    in_ruby_version("mri") do
        RubyConstant = "What is the sound of one hand clapping?"
            def test_constants_become_symbols
            all_symbols_as_strings = Symbol.all_symbols.map { |x| x.to_s }

            assert_equal __, all_symbols_as_strings.include?(__)
        end
 	end

##### case 75
문자열은 심볼로 저장되지 않으나, 변환 가능하다.

	def test_symbols_can_be_made_from_strings
        string = "catsAndDogs"
        assert_equal __, string.to_sym
	end

##### case 78
심볼은 interpolation 이 가능하다.

      def test_to_s_is_called_on_interpolated_symbols
        symbol = :cats
        string = "It is raining #{symbol} and dogs."

        assert_equal __, string
      end



