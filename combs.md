# Egel interpreter builtin combinators

## system

The 'system' module defines primitive combinators.

 + `System::k` *x y* -  k combinator

 + `System::id` *x* -  identity combinator

 + `System::max_int` -  maximum for integers

 + `System::+` *x y* -  addition

 + `System::!-` *x* -  monadic minus

 + `System::+` *x y* -  substraction

 + `System::*` *x y* -  multiplication

 + `System::/` *x y* -  division

 + `System::%` *x y* -  modulo

 + `System::<` *x y* -  builtin less

 + `System::<=` *x y* -  builtin less or equals

 + `System::>` *x y* -  builtin greater

 + `System::>=` *x y* -  builtin greater or equals

 + `System::==` *x y* -  builtin equality

 + `System::/=` *x y* -  builtin inequality

 + `System::&` *x y* -  bitwise and

 + `System::$` *x y* -  bitwise or

 + `System::^` *x y* -  bitwise xor

 + `System::!~` *x* -  bitwise complement

 + `System::<<` *x y* -  bitwise left shift

 + `System::>>` *x y* -  bitwise right shift

 + `System::to_int` *x* -  Try and convert an object to int

 + `System::to_float` *x* -  try and convert an object to float

 + `System::to_text` *x* -  try and convert an object to text

 + `String::to_chars` *s* -  create a list of chars from a string

 + `String::from_chars` *s* -  create a string from a list of chars

 + `System::version` -  version information of this executable

 + `System::arg` *n* -  the n-th application argument, or none

 + `System::get_env` *s* -  the value of environment variable, or none

 + `System::args_to_list` *o0 .. on* -  arguments to list

 + `System::list_to_app` *{o0 .. on}* -  list to application

 + `System::print` *o0 .. on* -  print terms

 + `System::get_line` -  read a line from standard input

 + `System::format` *fmt x0 ...* -  create a formatted strin

 + `System::ref` *x* -  create a reference object

 + `System::set_ref` *ref x* -  set reference objec

 + `System::get_ref` *ref* -  dereference

## math

The 'math' module defines trigonometic and some other often used combinators.

 + `Math::e` -  Euler's constant and the base of natural logarithms,

 + `Math::ln2` -  Natural logarithm of 2, approximately 0.693

 + `Math::ln10` -  natural logarithm of 10, approximately 2.303

 + `Math::log2e` -  base 2 logarithm of E, approximately 1.443

 + `Math::log10e` -  base 10 logarithm of E, approximately 0.434

 + `Math::pi` -  ratio of the circumference of a circle to its diameter,

 + `Math::sqrt1_2` -  square root of 1/2; equivalently, 1 over the square root

 + `Math::sqrt2` -  square root of 2, approximately 1.414

 + `Math::abs` *x* -  the absolute value of a number

 + `Math::acos` *x* -  the arccosine of a number

 + `Math::acosh` *x* -  the hyperbolic arccosine of a number

 + `Math::asin` *x* -  the arcsine of a number

 + `Math::asinh` *x* -  the hyperbolic arcsine of a number

 + `Math::atan` *x* -  the arctangent of a number

 + `Math::atanh` *x* -  the hyperbolic arctangent of a number

 + `Math::atan2` *y x* -  the arctangent of the quotient of its arguments

 + `Math::cbrt` *x* -  the cube root of a number

 + `Math::ceil` *x* -  the ceiling of a number

 + `Math::cos` *x* -  the cosine of a number

 + `Math::cosh` *x* -  the hyperbolic cosine of a number

 + `Math::exp` *x* -  the exp of a number

 + `Math::expm1` *x* -  subtracting 1 from exp

 + `Math::floor` *x* -  the largest integer less than or equal to a number

 + `Math::log` *x* -  the natural logarithm (loge, also ln) of a number

 + `Math::log1p` *x* -  the natural logarithm of the next number

 + `Math::log10` *x* -  the base 10 logarithm of a number

 + `Math::log2` *x* -  the base 2 logarithm of a number

 + `Math::max` *x y* -  the largest of two numbers

 + `Math::min` *x y* -  the smallest of two numbers

 + `Math::pow` *x y* -  base to the exponent power, that is, baseexponent

 + `Math::random` -  a pseudo-random number between 0 and 1

 + `Math::round` *x* -  the value of a number rounded to the nearest

 + `Math::sign` *x* -  the sign of the a number

 + `Math::sin` *x* -  the sine of a number

 + `Math::sinh` *x* -  the hyperbolic sine of a number

 + `Math::sqrt` *x* -  the positive square root of a number

 + `Math::tan` *x* -  the tangent of a number

 + `Math::tanh` *x* -  the hyperbolic tangent of a number

 + `Math::trunc` *x* -  the integral part of a number

## string

The 'string' module defines string manipulation combinators.

 + `String::eq` *s0 s1* -  string equality operator

 + `String::neq` *s0 s1* -  inequality operator

 + `String::gt` *s0 s1* -  greater than operator

 + `String::ls` *s0 s1* -  less than operator

 + `String::ge` *s0 s1* -  greater than or equal operator

 + `String::le` *s0 s1* -  stringLess than or equal operator

 + `String::compare` *s0 s1* -  compare the characters bitwise

 + `String::compare_order` *s0 s1* -  compare in code point order

 + `String::case_compare` *s0 s1* -  compare two strings case-insensitivel

 + `String::extract` *n0 n1 s* -  extract range of chars from text

 + `String::starts_with` *s0 s1* -  starts with initial segment

 + `String::ends_with` *s0 s1* -  ends with segment

 + `String::index_of` *s0 s1* -  the first occurrence of a text

 + `String::last_index_of` *s0 s1* -  the last occurrence of a text

 + `String::char_at` *n s* -  the char at offset

 + `String::move_index` *index delta s* -  move index by delta chars

 + `String::count` *s* -  number of chars

 + `String::is_empty` *s* -  test whether the text is empty

 + `String::hash_code` *s* -  generate a hash code for this text

 + `String::is_bogus` *s* -  determine if this object contains a valid string

 + `String::append` *s0 s1* -  append two texts

 + `String::insert` *s0 n s1* -  insert at given position

 + `String::replace` *s0 s1 s2* -  replace all occurrences

 + `String::remove` *n0 n1 s* -  remove characters in range

 + `String::retain` *n0 n1 s* -  retain the characters in the range

 + `String::trim` *s* -  trims leading and trailing whitespac

 + `String::reverse` *s* -  reverse

 + `String::to_upper` *s* -  convert to upper case

 + `String::to_lower` *s* -  convert to lower case

 + `String::fold_case` *s* -  case-folds the character

 + `String::ord` *c* -  integer value of unicode point/character

 + `String::chr` *n* -  unicode point of integer value

 + `String::unescape` *s* -  unescape characters

## regex

The 'regex' module defines operations on regular expressions.

 + `Regex::compile` *s0* -  compile text to a pattern

 + `Regex::match` *pat s0* -  true if the pattern matches the entire string

 + `Regex::look_at` *pat s0* -  true if the pattern matches the start of string

 + `Regex::look_match` *pat s0* -  the initial matched part of the string

 + `Regex::split` *pat s0* -  split a text according to a pattern

 + `Regex::matches` *pat s0* -  a list of pattern matches in a string

 + `Regex::replace` *pat s0 s1* -  replace the first occurence of a pattern

 + `Regex::replace_all` *pat s0 s1* -  replace all occurences of a pattern 

 + `Regex::group` *pat s0* -  the matched groups in a string

## dict

The 'dict' module defines mutable dictionaries.

 + `Dict::dict` -  create a dict object

 + `Dict::has` *d k* -  check for key

 + `Dict::get` *d k* -  get a value by key

 + `Dict::set` *d k v* -  set a value by key

 + `Dict::erase` *d k* -  erase a value by key

 + `Dict::keys` *d* -  dictionary keys as list

## async

The 'async' module defines concurrency combinators.

 + `System::async` *f* -  create a task

 + `System::await` *f* -  wait for async task

 + `System::wait_for` *f n* -  check whether future reduced during milliseconds

 + `System::is_valid` *f* -  check whether future is reduced

 + `System::sleep` *n* -  sleep for a number of milliseconds

## eval

The 'eval' module defines the eval combinator.

 + `System::eval` *text* -  evaluatate the expression in `text`

## runtime

The 'runtime' module provides binding to the runtime.

 + `System::dis` *o* -  disassemble a combinator object

 + `System::asm` *s* -  assemble bytecode into a combinator

 + `System::serialize` *t* -  serialize a term to a text

 + `System::deserialize` *t* -  serialize a text to a term

 + `System::docstring` *o* -  docstring of a module or combinator

 + `System::query_modules` -  list all modules in the runtime

 + `System::is_module` *m* -  check we have a module

 + `System::query_module_name` *m* -  get the name of the module

 + `System::query_module_path` *m* -  get the path of the module

 + `System::query_module_imports` *m* -  get the imports of the module

 + `System::query_module_exports` *m* -  get the exports of the module

 + `System::query_module_values` *m* -  get the values of the module

## time

The 'time' module defines time and date combinators.

 + `Time::clock` *s* -  create a clock object

 + `Time::now` *c* -  current time according to a clock

 + `Time::is_steady` *c* -  is a steady clock

 + `Time::milliseconds` *n* -  a number of milliseconds

 + `Time::seconds` *n* -  a number of seconds

 + `Time::minutes` *n* -  a number of minutes

 + `Time::hours` *n* -  a number of hours

 + `Time::days` *n* -  a number of days

 + `Time::weeks` *n* -  a number of weeks

 + `Time::months` *n* -  a number of months

 + `Time::years` *n* -  a number of years

 + `Time::local_time` *n* -  time point to local date

 + `Time::gm_time` *n* -  time point to gm date

 + `Time::date_to_time` *n* -  date to time point

 + `Time::date_to_tuple` *n* -  date to tuple

 + `Time::date_from_tuple` *n* -  date from tuple

## ffi

The 'ffi' module defines c foreign interface combinators.

 + `FFI::load_library` *s* -  load a library

 + `FFI::function` *l s* -  find a function

 + `FFI::call` *f r x* -  call a function

 + `FFI::malloc` *n* -  allocate a number of bytes

 + `FFI::free` *p* -  free memory

 + `FFI::peek` *p n t* -  peek a number of bytes beyond for value of type

 + `FFI::poke` *p n v* -  poke a value a number of bytes beyond pointer

 + `FFI::to_utf8` *s* -  get pointer from text

 + `FFI::from_utf8` *s* -  get text from pointer

## os

The 'os' module defines basic input/output combinators.

 + `OS::cin` -  standard input channel

 + `OS::stdout` -  standard output channel

 + `OS::stderr` -  standard error channel

 + `OS::open_in` *fn* -  create a channel from filename

 + `OS::open_out` *fn* -  create a channel from filename

 + `OS::close` *c* -  close a channel

 + `OS::read` *c* -  read a string from a channel

 + `OS::read_byte` *c* -  read a byte from a channel

 + `OS::read_line` *c* -  read a line from a channel

 + `OS::read_all` *c* -  read entire channel content

 + `OS::write` *c s* -  write a string to a channel

 + `OS::write_byte` *c b* -  write a byte to a channel

 + `OS::write_line` *c s* -  write a string s to a channel

 + `OS::flush` *c* -  flush a channel

 + `OS::eof` *c* -  tests if there is no more input

 + `OS::flock` *f n* -  create a filesystem lock file (not process safe)

 + `OS::exit` *n* -  flush all channels and terminate process with exit code n

 + `OS::exec` *c* -  system exec command

 + `OS::get_key` -  key press from console

## fs

The 'fs' module defines file system inspection and modification combinators.

 + `OS::concat` *p0 p1* -  concatenates two paths

 + `OS::concat_with` *p0 p1* -  concatenates two paths with a directory separator

 + `OS::empty` *p* -  checks whether the path is empty

 + `OS::has_root_path` *p* -  checks whether the path has a root path

 + `OS::has_root_name` *p* -  checks whether path has a root name

 + `OS::has_root_directory` *p* -  checks whether the path has a root directory

 + `OS::has_relative_path` *p* -  checks whether the path has a relative path

 + `OS::has_parent_path` *p* -  checks whether the path has a parent path

 + `OS::has_filename` *p* -  checks whether the path has a filename

 + `OS::has_stem` *p* -  checks whether the path has a stem

 + `OS::has_extension` *p* -  checks whether the path has an extension

 + `OS::is_absolute` *p* -  checks whether the path is absolute

 + `OS::is_relative` *p* -  checks whether the path is relative

 + `OS::root_name` *p* -  returns the root-name of the path, if present

 + `OS::root_directory` *p* -  returns the root directory of the path, if present

 + `OS::root_path` *p* -  returns the root path of the path, if present

 + `OS::relative_path` *p* -  returns path relative to the root path

 + `OS::parent_path` *p* -  returns the path of the parent path

 + `OS::filename` *p* -  returns the filename path component

 + `OS::stem` *p* -  returns the stem path component

 + `OS::extension` *p* -  returns the file extension path component

 + `OS::absolute` *p* -  composes an absolute path

 + `OS::copy` *src dst* -  copies files or directories

 + `OS::copy_file` *src dst* -  copies file contents

 + `OS::copy_symlink` *src trg* -  copies a symbolic link

 + `OS::create_directory` *p* -  creates new directory

 + `OS::create_directories` *p* -  creates new directories

 + `OS::create_hard_link` *p0 p1* -  creates a hard link

 + `OS::create_symlink` *p0 p1* -  creates a symbolic link

 + `OS::create_directory_symlink` *p0 p1* -  creates a symbolic link

 + `OS::current_path` -  returns the current working directory

 + `OS::set_current_path` *p* -  sets the current working directory

 + `OS::exists` *p* -  checks whether path refers to existing file system object

 + `OS::equivalent` *p0 p1* -  checks whether two paths refer to the same file

 + `OS::file_size` *p* -  returns the size of a file

 + `OS::hard_link_count` *p* -  returns the number of hard links 

 + `OS::permissions` *p* -  get file access permissions

 + `OS::replace_permissions` *p n* -  set file access permissions

 + `OS::read_symlink` *p* -  obtains the target of a symbolic link

 + `OS::remove` *p* -  removes a file or empty directory

 + `OS::remove_all` *p* -  removes a file or directory and all its contents

 + `OS::rename` *p0 p1* -  moves or renames a file or directory

 + `OS::resize_file` *p n* -  changes the size of a regular file 

 + `OS::space_free` *p* -  determines free space on the file system

 + `OS::space_capacity` *p* -  determines capacity space on the file system

 + `OS::space_available` *p* -  determines available space on the file system

 + `OS::temp_directory_path` -  returns a directory suitable for temporary files

 + `OS::is_block_file` *p* -  checks whether the given path refers to block device

 + `OS::is_character_file` *p* -  the given path refers to a character device

 + `OS::is_directory` *p* -  checks whether the given path refers to a directory

 + `OS::is_empty` *p* -  checks whether the given path refers to an empty file or

 + `OS::is_fifo` *p* -  checks whether the given path refers to a named pipe

 + `OS::is_other` *p* -  checks whether the argument refers to an other file

 + `OS::is_regular_file` *p* -  the argument refers to a regular file

 + `OS::is_socket` *p* -  checks whether the argument refers to a named IPC socket

 + `OS::is_symlink` *p* -  checks whether the argument refers to a symbolic link

 + `OS::directory` *p* -  lists the content of a directory

## random

The 'random' module defines randomization combinators. (Work in progress)

 + `Math::between` *min max* -  a random number between min and max

## prelude.eg

The 'prelude' defines often used combinators.


 + `System::or` *p q* -  boolean or

 + `System::and` *p q* -  boolean and

 + `System::not` *p q* -  boolean not

 + `System::||` *p q* -  'lazy' or

 + `System::&&` *p q* -  'lazy' and

 + `System::fix` *f* -  fixed point of f

 + `System::.` *f g* -  function composition

 + `System::|>` *x f* -  reverse application

 + `System::||>` *x f* -  reverse application ignoring none

 + `System::@` *f x* -  low binding application

 + `System::flip` *f x y* -  flip two arguments

 + `System::join` *f x* -  f x x

 + `System::uncurry` *f (x, y)* -  uncurry arguments

 + `System::iter` *n f x* -  iterate a function

 + `System::trace` *n f x* -  trace iteration of a function

 + `System::trace_until` *f g x* -  trace until a guard holds

 + `System::trace_while` *f g x* -  trace while a guard holds

 + `System::while` *f x* -  apply f as long as it reduces

 + `System::swap` *(x,y)* -  swap a tuple

 + `System::proj` *n (x, .., y)* -  projection on tuple

 + `System::fst` *(x, y)* -  proj1 on tuple

 + `System::snd` *(x, y)* -  proj2 on tuple

 + `System::abs` *x* -  absolute

 + `System::min` *x y* -  minimum

 + `System::max` *x y* -  maximum

 + `System::**` *x y* -  power (temporary)

 + `System::printf` *s x0 .. xn* -  print formatted

 + `List::length` *l* -  length of a list

 + `List::foldl` *f z l* -  left fold on a list

 + `List::foldr` *f z l* -  right fold on a list

 + `List::scanl` *f z l* -  left scan on a list

 + `List::reduce` *f l* -  reduce on non-empty list

 + `List::head` *l* -  head of a list

 + `List::tail` *l* -  tail of a list

 + `List::last` *l* -  last of a list

 + `List::init` *l* -  init of a list

 + `List::inits` *l* -  inits of a list

 + `List::tails` *l* -  tails of a list

 + `List::++` *l0 l1* -  concatenation of two lists

 + `List::postpend` *l e* -  postpend an element

 + `List::map` *f l* -  map a function over a list

 + `List::concat_map` *f l* -  map a function producing lists over a list

 + `List::reverse` *l* -  reverse a list

 + `List::block` *n* -  list of number from 0 to n exclusive

 + `List::repeat` *n x* -  list of n x elements

 + `List::power` *l* -  powerset of a list

 + `List::pairs` *ll0 ll1* -  product of two lists

 + `List::combine` *ll* -  all lists that are the product of the members of a list of lists

 + `List::nth` *n l* -  nth element of a list

 + `List::index_of` *x xx* -  index of a member in list

 + `List::insert` *n x l* -  insert an element at given position

 + `List::take` *n l* -  take the first elements of a list

 + `List::drop` *n l* -  drop the first elements of a list

 + `List::split_at` *n l* -  take and drop the first elements of a list

 + `List::chunks` *n l* -  list to list of chunks of given size

 + `List::from_to` *l u* -  list of numbers for lower to upper (inclusive)

 + `List::filter` *p l* -  filter all members from a list which satisfy a predicate

 + `List::split` *p l* -  split a list into members and non-members of a predicate

 + `List::break` *p l* -  split a list in two parts

 + `List::split_on` *x ll* -  split a list on a member

 + `List::flatten` *ll* -  flatten a list of lists to a list

 + `List::zip` *l0 l1* -  zip two lists to a list of pairs

 + `List::zip_with` *f l0 l1* -  apply a function pairwise to members of two lists

 + `List::transpose` *ll* -  transpose a list of lists

 + `List::any` *p l* -  checks whether any element of a list satisfies a predicate

 + `List::all` *p l* -  checks whether all elements of a list  satisfies a predicate

 + `List::elem` *x l* -  membership test

 + `List::not_elem` *x l* -  inverse membership test

 + `List::union` *l0 l1* -  union of two lists (nˆ2 complexity)

 + `List::intersection` *l0 l1* -  intersection of two lists (nˆ2 complexity)

 + `List::difference` *l0 l1* -  intersection of two lists (nˆ2 complexity)

 + `List::insert_everywhere` *x l* -  insert a member in every position of a list

 + `List::permutations` *l* -  all permutations of a list

 + `List::sort` *l* -  merge sort 

 + `List::sort_by` *f l* -  merge sort with an order operator

 + `List::nub` *l* -  remove consecutive duplicates

 + `List::group` -  group duplicates

 + `List::unique` *l* -  make all members unique

 + `List::sum` *l* -  summation of list

 + `List::product` *l* -  product of list

 + `List::maximum` *l* -  maximum of list

 + `List::minimum` *l* -  minimum of list

 + `List::range` *l f* -  iterate over elements (reverse map

 + `List::range2` *l0 l1 f* -  iterate over elements of two lists

 + `List::range3` *l0 l1 l2 f* -  iterate over elements of three lists

 + `System::args` -  arguments of the application

 + `String::split` *n s* -  split a spring

 + `Math::lift_unary` *f* -  lift a unary function on floats to ints

 + `Math::lift_binary` *f* -  lift a binary function on floats to ints

 + `Math::pow_int` *n0 n1* -  power of two integer values

 + `System::help_exact_matches` *s* -  return a list of exact docstring matches

 + `System::help_inexact_matches` *s* -  return a list of inexact docstring matches

 + `System::help` -  search for information

## calculate.eg

Calculations are small abstractions where some computation is done
modulo some state.

All calculations are chained actions. An action is a function which 
gets as an arguments a state and returns a tuple of a result and a
state.


 + `Calculate::return` *a* -  calculate further with value

 + `Calculate::chain` *f g* -  chain two calculations

 + `Calculate::run` *f s* -  run calculation on state

 + `Calculate::<*` *f g* -  chain

 + `Calculate::skip` -  return a none

 + `Calculate::apply` *f g* -  apply a function to a calculation

 + `Calculate::modify` *f g* -  modify state

 + `Calculate::<@` *f g* -  apply

 + `Calculate::<+` *f g* -  modify

## search.eg

Searching is calculation over a state, minimalist theory.

 + `Search::success` *a* -  succeed with value a

 + `Search::fail` -  fail an alternative

 + `Search::raise` -  fail all alternatives

 + `Search::message` *m* -  fail or raise with message

 + `Search::parallel` *p q* -  try both alternatives

 + `Search::sequential` -  try alternatives sequentially

 + `Search::serial` *p q* -  try alternative, then force the next

 + `Search::apply` *p f* -  apply to the argument being calculated

 + `Search::opt` *p v* -  optionally succeed with a value

 + `Search::serial_opt` *p q* -  optionally succeed with value

 + `Search::<+>` *p q* -  try both alternatives  

 + `Search::<->` *p q* -  try composition of alternatives

 + `Search::<*>` *p q* -  try alternative then force

 + `Search::</>` *p q* -  try alternative then optionally

 + `Search::<@>` *p f* -  apply function to the result

 + `Search::<!>` *p m* -  set the failure message

 + `Search::one` *p* -  one time and return a singleton result

 + `Search::plus` *p* -  one or more and return a list result

 + `Search::star` *p* -  zero or more and return a list result

 + `Search::plus_sep` *p s* -  one or more with separator

 + `Search::star_sep` *p s* -  zero or more with separator

 + `Search::search` *p f t e s* -  search on state with three handlers

## generator.eg

Generators model infinite list structures.

 + `Gen::to_list` *g* -  generator to list

 + `Gen::from_list` *l* -  list to generator

 + `Gen::length` *l* -  length of a list

 + `Gen::foldl` *f z l* -  left fold on a list

 + `Gen::foldr` *f z l* -  right fold on a list

 + `Gen::head` *l* -  head of a list

 + `Gen::tail` *l* -  tail of a list

 + `Gen::++` *l0 l1* -  concatenation of two lists

 + `Gen::map` *f l* -  map a function over a list

 + `Gen::reverse` *l* -  reverse a list

 + `Gen::block` *n* -  list of number from lower to upper exclusive

 + `Gen::nth` *n l* -  nth element of a list

 + `Gen::insert` *n x l* -  insert an element at given position

 + `Gen::take` *n l* -  take the first elements of a list

 + `Gen::drop` *n l* -  drop the first elements of a list

 + `Gen::repeat` *n* -  infinite list of elements

 + `Gen::cycle` *l* -  infinite list of cycling list

 + `Gen::from` *min* -  list of numbers from min 

 + `Gen::from_to` *min max* -  list of numbers for min to max (exclusive)

 + `Gen::filter` *p l* -  filter all members from a list which satisfy a predicate

 + `Gen::flatten` *ll* -  flatten a list of lists to a list

 + `Gen::zip` *l0 l1* -  zip to lists to a list of pairs

 + `Gen::zip_with` *f l0 l1* -  apply a function pairwise to members of two lists

 + `Gen::any` *p l* -  checks whether any element of a list satisfies a predicate

 + `Gen::all` *p l* -  checks whether all elements of a list  satisfies a predicate

 + `Gen::elem` *x l* -  membership test

 + `Gen::not_elem` *x l* -  inverse membership test

 + `Gen::from_lists` *l* -  convert a list of lists to generator of generators

 + `Gen::to_lists` *c* -  convert generator of generators to list of lists

 + `Gen::space` -  space, the final frontier

 + `Gen::map_2d` -  map on a space

 + `Gen::take_2d` -  take a block 

 + `Gen::range` *l f* -  iterate over elements (reverse map

 + `Gen::range2` *l0 l1 f* -  iterate over elements of two lists

 + `Gen::range3` *l0 l1 l2 f* -  iterate over elements of three lists

