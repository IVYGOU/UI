## What Should You Test?
* Test all the public functions you introduced.
* Test all the overwritten getters and setters.
* Test your control's events and how often they are called.
* Test all possible user interactions (tap, keyboard, focus).
* You could test how often your control gets rerendered when interacting with it, but only if you are worried that it might be rerenderd too often or not at all.
* Test RTL if you have special things done in javascript.
* Write some integration tests if you have a composite control (don't cover 100% of your child controls - that's overkill and child controls will be hard to maintain).
* You may test default values of properties, since we cannot change them backwards compatible and a test will recognize this.
* Test how your control interacts with models (OData + Json).
* Test the destruction of your control when working with composites, test if all dependencies/events are unbound on destruction.

## What Should You NOT Test?
* Never test non-overwritten getters and setters (these are tested in the core of the framework).
* Never test your complete css with computed styles: just check if the classes are set correctly. Focus on testing javascript.
* Never test other generic framework functionality: focus on your control.
