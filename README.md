# Convert-string-to-camel-case

My Solution::

function toCamelCase($str){

 $str = implode('-', array_map('ucfirst', explode('-', $str)));
 $str = preg_replace('/[_-]/','', ucwords($str));
  
  
 return $str;
}
echo toCamelCase("the-stealth-warrior"); // returns "theStealthWarrior"
echo toCamelCase("The_Stealth_Warrior"); // returns "TheStealthWarrior"

Output::

TheStealthWarrior
TheStealthWarrior

Correct Output Should::

theStealthWarrior
TheStealthWarrior


