**An implementation of the PHP date() Function in ActionScript3**

## Short Instruction: ##
### Use instance of PhpDate Class ###
```
var phpDate:PhpDate = new PhpDate();
//or var phpDate:PhpDate = new PhpDate( 1211528051 );
//or var phpDate:PhpDate = new PhpDate( new Date() );
trace( phpDate.format( "H:i" ) );
```
In this variant you can give over the constructor a string parameter, containing an unix-timestamp. As default it will use the current date-time.

### Use the static method ###
This method always use the current time given by the AS3-Date Object.
```
PhpDate.format( "r" );
PhpDate.format( "r", 1211528051 );
PhpDate.format( "r", new Date() );
```