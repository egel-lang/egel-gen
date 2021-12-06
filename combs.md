# Egel interpreter builtin combinators

## <egel/src/builtin_system.cpp>

 + `System::k` *x y* - k combinator

 + `System::id` *x* - identity combinator

 + `System::!-` *x* - monadic minus

 + `System::+` *x y* - addition

 + `System::+` *x y* - substraction

 + `System::*` *x y* - multiplication

 + `System::/` *x y* - division

 + `System::%` *x y* - modulo

 + `System::&` *x y* - bitwise and

 + `System::$` *x y* - bitwise or

 + `System::^` *x y* - bitwise xor

 + `System::!~` *x* - bitwise complement

 + `System::<<` *x y* - bitwise left shift

 + `System::>>` *x y* - bitwise right shift

 + `System::<` *x y* - builtin less

 + `System::<=` *x y* - builtin less or equals

 + `System::==` *x y* - builtin equality

 + `System::/=` *x y* - builtin inequality

 + `System::get` *field obj* - retrieve an object field

 + `System::set` *field val obj* - set an object field

 + `System::extend` *obj0 obj1* - extend object obj0 with every field from obj1

 + `System::to_int` *x* - Try and convert an object to int

 + `System::to_float` *x* - try and convert an object to float

 + `System::to_text` *x* - try and convert an object to text

 + `System::ref` *x* - create a reference object from x

 + `System::get_ref` *ref* - get the stored value from ref

 + `System::set_ref` *ref x* - set reference object ref to x

 + `System::unpack` *s* - create a list of chars from a string

 + `System::pack` *s* - create a string from a list of code points

 + `System::arg` *n* - return the n-th application argument, otherwise return 'none'

 + `System::get_env` *s* - return the value of environment variable s, otherwise return 'none'

 + `System::print` *o0 .. on* - print terms, don't escape characters or texts 

 + `System::format` *fmt x ... * - create a string from formatted string fmt and objects x,..

## <egel/src/builtin_math.cpp>

 + `Math::is_finite` *x* - test whether this float is finite

 + `Math::is_infinite` *x* - test whether this float is infinite

 + `Math::is_nan` *x* - test whether this float is Not a Number

 + `Math::is_normal` *x* - test whether this float is normal

 + `Math::abs` *x* - returns the absolute value of a number

 + `Math::acos` *x* - returns the arccosine of a number

 + `Math::acosh` *x* - returns the hyperbolic arccosine of a number

 + `Math::asin` *x* - returns the arcsine of a number

 + `Math::asinh` *x* - returns the hyperbolic arcsine of a number

 + `Math::atan` *x* - returns the arctangent of a number

 + `Math::atanh` *x* - returns the hyperbolic arctangent of a number

 + `Math::atan2` *y x* - returns the arctangent of the quotient of its arguments

 + `Math::cbrt` *x* - returns the cube root of a number

 + `Math::ceil` *x* - returns the smallest integer greater than or equal to a number

 + `Math::cos` *x* - returns the cosine of a number

 + `Math::cosh` *x* - returns the hyperbolic cosine of a number

 + `Math::exp` *x* - Returns Ex, where x is the argument, and E is Euler's constant (2.718…), the base of the natural logarithm

 + `Math::expm1` *x* - returns subtracting 1 from exp x

 + `Math::floor` *x* - returns the largest integer less than or equal to a number

 + `Math::log` *x* - returns the natural logarithm (loge, also ln) of a number

 + `Math::log1p` *x* - returns the natural logarithm (loge, also ln) of 1 + x for a number x

 + `Math::log10` *x* - returns the base 10 logarithm of a number

 + `Math::log2` *x* - returns the base 2 logarithm of a number

 + `Math::max` *x y* - returns the largest of two numbers

 + `Math::min` *x y* - returns the smallest of two numbers

 + `Math::pow` *x y* - returns base to the exponent power, that is, baseexponent

 + `Math::round` *x* - returns the value of a number rounded to the nearest integer

 + `Math::sign` *x* - returns the sign of the x, indicating whether x is positive, negative or zero

 + `Math::sin` *x* - returns the sine of a number

 + `Math::sinh` *x* - returns the hyperbolic sine of a number

 + `Math::sqrt` *x* - returns the positive square root of a number

 + `Math::tan` *x* - returns the tangent of a number

 + `Math::tanh` *x* - returns the hyperbolic tangent of a number

 + `Math::trunc` *x* - returns the integral part of the number x, removing any fractional digits

## <egel/src/builtin_eval.cpp>

 + `System::eval` *text* - evaluatate the expression in `text`

## <egel/src/builtin_string.cpp>

 + `String::eq` *s0 s1* - string equality operator

 + `String::neq` *s0 s1* - inequality operator

 + `String::gt` *s0 s1* - greater than operator

 + `String::ls` *s0 s1* - string less than operator

 + `String::ge` *s0 s1* - greater than or equal operator

 + `String::le` *s0 s1* - stringLess than or equal operator

 + `String::compare` *s0 s1* - compare the characters bitwise in this icu::UnicodeString to the characters in text

 + `String::compare_order` *s0 s1* - compare two Unicode strings in code point order

 + `String::case_compare` *s0 s1* - compare two strings case-insensitively using full case folding

 + `String::starts_with` *s0 s1* - determine if this starts with the characters in text 

 + `String::ends_with` *s0 s1* - determine if this ends with the characters in text 

 + `String::index_of` *s0 s1* - locate in this the first occurrence of the characters in text, using bitwise comparison

 + `String::last_index_of` *s0 s1* - locate in this the last occurrence of the characters in text, using bitwise comparison

 + `String::char_at` *n s* - return the code point that contains the code unit at offset offset

 + `String::move_index` *index delta s* - move the code unit index along the string by delta code points

 + `String::count_char` *s* - count Unicode code points in the string

 + `String::is_empty` *s* - test whether the string is empty

 + `String::hash_code` *s* - generate a hash code for this object

 + `String::is_bogus` *s* - determine if this object contains a valid string

 + `String::append` *s0 s1* - append the two strings

 + `String::insert` *s0 n s1* - insert the characters in s0 into the s1 at offset n

 + `String::replace` *s0 s1 s2* - replace all occurrences of characters s0 with the characters s2 in s0

 + `String::remove` *n0 n1 s* - remove the characters in the range [n0, n1) from s

 + `String::retain` *n0 n1 s* - retain the characters in the range [n0, n1) from s

 + `String::trim` *s* - trims leading and trailing whitespace from this s 

 + `String::reverse` *s* - reverse s

 + `String::to_upper` *s* - convert the characters in this to upper case following the conventions of the default locale

 + `String::to_lower` *s* - convert the characters in this to lower case following the conventions of the default locale

 + `String::fold_case` *s* - case-folds the characters in this string

 + `String::unescape` *s* - unescape a string of characters and return a string containing the result

 + `String::ord` *c* - integer value of unicode point/character

 + `String::chr` *n* - unicode point of integer value

## <egel/src/builtin_eval.cpp>

 + `System::eval` *text* - evaluatate the expression in `text`

## <egel/src/builtin_thread.cpp>

 + `System::par` *f g* - concurrently evaluate 'f none' and 'g none'

## <egel/src/builtin_process.cpp>

 + `System::proc` *f* - create a process object from f

 + `System::send` *proc msg* - send message msg to proc

 + `System::recv` *proc* - receive a message from process proc

 + `System::halt` *proc* - halt process proc

## <egel/lib/os/os.cpp>

 + `OS::open` *fn* - create a channel from filename 

 + `OS::close` *c* - close a channel

 + `OS::read` *c* - read a string from a channel

 + `OS::read_line` *c* - read a line from a channel

 + `OS::write` *c s* - write a string s to a channel

 + `OS::write_line` *c s* - write a string s to a channel

 + `OS::flush` *c* - flush a channel

 + `OS::eof` *c* - tests if there is no more input

 + `OS::exit` *n* - flush all channels and terminate process with exit code n

 + `OS::accept` *serverobject* - accept connections

 + `OS::server` *port in* - create a serverobject 

 + `OS::client` *host port* - create a client channel

## <egel/lib/fs/fs.cpp>

 + `OS::empty` *p* - checks whether the path is empty

 + `OS::has_root_path` *p* - checks whether the path has a root path

 + `OS::has_root_name` *p* - checks whether path has a root name

 + `OS::has_root_directory` *p* - checks whether the path has a root directory

 + `OS::has_relative_path` *p* - checks whether the path has a relative path

 + `OS::has_parent_path` *p* - checks whether the path has a parent path

 + `OS::has_filename` *p* - checks whether the path has a filename

 + `OS::has_stem` *p* - checks whether the path has a stem

 + `OS::has_extension` *p* - checks whether the path has an extension

 + `OS::is_absolute` *p* - checks whether the path is absolute

 + `OS::is_relative` *p* - checks whether the path is relative

 + `OS::root_name` *p* - returns the root-name of the path, if present

 + `OS::root_directory` *p* - returns the root directory of the path, if present

 + `OS::root_path` *p* - returns the root path of the path, if present

 + `OS::relative_path` *p* - returns path relative to the root path

 + `OS::parent_path` *p* - returns the path of the parent path

 + `OS::filename` *p* - returns the filename path component

 + `OS::stem` *p* - returns the stem path component

 + `OS::extension` *p* - returns the file extension path component

 + `OS::absolute` *p* - composes an absolute path

 + `OS::copy` *src dst* - copies files or directories

 + `OS::copy_file` *src dst* - copies file contents

 + `OS::copy_symlink` *src trg* - copies a symbolic link

 + `OS::create_directory` *p* - creates new directory

 + `OS::create_directories` *p* - creates new directories

 + `OS::create_hard_link` *p0 p1* - creates a hard link

 + `OS::create_symlink` *p0 p1* - creates a symbolic link

 + `OS::create_directory_symlink` *p0 p1* - creates a symbolic link

 + `OS::set_current_path` *p* - sets the current working directory

 + `OS::exists` *p* - checks whether path refers to existing file system object

 + `OS::equivalent` *p0 p1* - checks whether two paths refer to the same file system object

 + `OS::file_size` *p* - returns the size of a file

 + `OS::hard_link_count` *p* - returns the number of hard links referring to the specific file

 + `OS::permissions` *p* - get file access permissions

 + `OS::replace_permissions` *p n* - set file access permissions

 + `OS::read_symlink` *p* - obtains the target of a symbolic link

 + `OS::remove` *p* - removes a file or empty directory

 + `OS::remove_all` *p* - removes a file or directory and all its contents, recursively

 + `OS::rename` *p0 p1* - moves or renames a file or directory

 + `OS::resize_file` *p n* - changes the size of a regular file by truncation or zero-fill

 + `OS::space_free` *p* - determines free space on the file system

 + `OS::space_capacity` *p* - determines capacity space on the file system

 + `OS::space_available` *p* - determines available space on the file system

 + `OS::is_block_file` *p* - checks whether the given path refers to block device

 + `OS::is_character_file` *p* - checks whether the given path refers to a character device

 + `OS::is_directory` *p* - checks whether the given path refers to a directory

 + `OS::is_empty` *p* - checks whether the given path refers to an empty file or directory

 + `OS::is_fifo` *p* - checks whether the given path refers to a named pipe

 + `OS::is_other` *p* - checks whether the argument refers to an other file

 + `OS::is_regular_file` *p* - checks whether the argument refers to a regular file

 + `OS::is_socket` *p* - checks whether the argument refers to a named IPC socket

 + `OS::is_symlink` *p* - checks whether the argument refers to a symbolic link

 + `OS::directory` *p* - lists the content of a directory

## <egel/lib/regex/regex.cpp>

 + `Regex::compile` *s0* - compile text to a pattern

 + `Regex::match` *pat s0* - true if the pattern matches the entire string

 + `Regex::look_at` *pat s0* - true if the pattern matches the start of string

 + `Regex::look_match` *pat s0* - returns the initial matched part of the string, or none

 + `Regex::split` *pat s0* - split a text according to a pattern

 + `Regex::matches` *pat s0* - return a list of pattern matches in a string

 + `Regex::replace` *pat s0 s1* - replace the first occurence of pattern in a string with a string

 + `Regex::replace_all` *pat s0 s1* - replace the all occurences of pattern in a string with a string

 + `Regex::group` *pat s0* - return the matched groups in a string

## <egel/lib/random/random.cpp>

 + `Math::between` *min max* - return a random number between min and max

## <egel/include/prelude.eg>

 + `System::or` *p q* - boolean or

 + `System::and` *p q* - boolean and

 + `System::not` *p q* - boolean not

 + `System::.` *f g* - function composition

 + `System::flip` *f x y* - flip two arguments

 + `System::uncurry` *f (x, y)* - uncurry arguments

 + `System::iter` *n f x* - iterate a function

 + `System::fst` *(x, y)* - proj0 on pair

 + `System::snd` *(x, y)* - proj1 on pair

 + `List::length` *l* - length of a list

 + `List::foldl` *f z l* - left fold on a list

 + `List::foldr` *f z l* - right fold on a list

 + `List::head` *l* - head of a list

 + `List::tail` *l* - tail of a list

 + `List::++` *l0 l1* - concatenation of two lists

 + `List::map` *f l* - map a function over a list

 + `List::reverse` *l* - reverse a list

 + `List::block` *n* - list of number from 0 to n exclusive

 + `List::nth` *n l* - nth element of a list

 + `List::insert` *n x l* - insert an element at given position

 + `List::take` *n l* - take the first n elements of a list

 + `List::drop` *n l* - drop the first n elements of a list

 + `List::from_to` *min max* - list of numbers for min to max (exclusive)

 + `List::filter` *p l* - filter all members from a list which satisfy a predicate

 + `List::split` *p l* - split a list into members and non-members of a predicate

 + `List::flatten` *ll* - flatten a list of lists to a list

 + `List::zip` *l0 l1* - zip to lists to a list of pairs

 + `List::zip_with` *f l0 l1* - apply a function pairwise to members of two lists

 + `List::transpose` *ll* - transpose a list of lists

 + `List::any` *p l* - checks whether any element of a list satisfies a predicate

 + `List::all` *p l* - checks whether all elements of a list  satisfies a predicate

 + `List::elem` *x l* - membership test

 + `List::not_elem` *x l* - inverse membership test

 + `List::union` *x l* - union of two lists (nˆ2 complexity)

 + `List::insert_everywhere` *x l* - insert a member in every position of a list

 + `List::concat_map` *f l* - concat map

 + `List::permutations` *l* - all permutations of a list

 + `List::sort` *l* - merge sort 

## <egel/include/calculate.eg>

 + `Calculate::return` *a* - calculate further with value a

 + `Calculate::chain` *f g* - first do f, then g

 + `Calculate::run` *f s* - run calculation f on state s

 + `Calculate::<*` *f g* - first do f, then g

 + `Calculate::apply` *f g* - first do f, then modify argument with g

 + `Calculate::modify` *f g* - first do f, then modify state with g

 + `Calculate::<@` *f g* - first do f, then apply g to argument

 + `Calculate::<+` *f g* - first do f, then modify state with g

## <egel/include/search.eg>

 + `Search::success` *a* - succeed with value a

 + `Search::message` *m* - fail or raise with message m

 + `Search::no_fail` *p* - this search may not fail

 + `Search::parallel` *p q* - try alternatives p or q

 + `Search::serial` *p q* - try alternative p then force q

 + `Search::apply` *p f* - apply f to the argument being calculated

 + `Search::opt` *p v* - optionally succeed p with value v

 + `Search::serial_opt` *p q* - optionally succeed p with value v

 + `Search::<+>` *p q* - try alternatives p or q

 + `Search::<+>` *p q* - try alternatives p then q

 + `Search::</>` *p q* - try alternatives p then q optionally

 + `Search::<*>` *p q* - try alternatives p then force q

 + `Search::<@>` *p f* - apply f to the result of p

 + `Search::<!>` *p m* - set the failure message to m

 + `Search::one` *p* - one time p and return a singleton result

 + `Search::plus` *p* - one or more p and return a list result

 + `Search::star` *p* - zero or more p and return a list result

 + `Search::plus_sep` *p s* - one or more p separated by s

 + `Search::star_sep` *p s* - zero or more p separated by s

 + `Search::search` *p s* - search with p on state s 

## <egel/include/map.eg>

 + `Map::empty_test` *m* - test for emptyness

 + `Map::choose` *m* - look at one key from the map

 + `Map::maximum` *m* - take the maximum key/value from the map

 + `Map::minimum` *m* - take the minimim key/value from the map

 + `Map::size` *m* - size of the map

 + `Map::look` *m k* - retrieve optional value from map with key

 + `Map::has` *m k* - check for key in map

 + `Map::member` *m k v* - check whether key/value is a member of map

 + `Map::nth` *m k* - take value from map with key

 + `Map::nth_total` *c m k* - take value from map with key or return constant

 + `Map::new_node` *k v l r* - create a new node

 + `Map::glue` *m0 m1* - glue two maps together

 + `Map::change` *f m* - change a map with a key and an update function (option value to option value)

 + `Map::insert` *k v m* - insert key/value into map

 + `Map::delete` *k m* - delete key from map

 + `Map::remove` *k v m* - remove key/value from map

 + `Map::foldr` *f c m* - foldr with key/value and accumulator function

 + `Map::foldl` *f c m* - foldl with key/value and accumulator function

 + `Map::foldm` *f c m* - foldm with key/value and accumulator function

 + `Map::apply` *f m* - map f to values in map

 + `Map::to_up_list` *m* - map to increasing list of key/value tuples

 + `Map::to_down_list` *f m* - map to decreasing list of key/value tuples

 + `Map::to_list` *m* - map to list

 + `Map::from_list` *l* - list to map

 + `Map::position` *m k* - position of key in map

 + `Map::domain` *m* - the keys in the map

 + `Map::range` *m* - the values in the map

 + `Map::any` *p m* - has a key/value in map satisfying predicate

 + `Map::all` *p m* - all key/value in map satisfy predicate

 + `Map::filter` *p m* - filter all key/value in map satisfy predicate

 + `Map::union` *m0 m1* - union of two maps

 + `Map::intersection` *m0 m1* - intersection of two maps

 + `Map::inverse` *m* - construct inverse of a map

 + `Map::compose` *m0 m1* - compose two maps

 + `Map::decompose` *m* - decompose a map into two maps with integers 

 + `Map::partition` *f m* - partition with a function which maps key/value to part

