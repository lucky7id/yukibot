## Bot Server

### Main Data Store
_Data hub that keeps track of module state. When a module attempts to connect
to the running bot, it will first register with this data store. During this
registration, lifecycle events such as auth and preboot will be fired. Any
dependencies the module requires will also be started if they are not already
running._

### Modules
_modules are the most ideal choice for allowing infinitely customizable server
deployments. A module can be something simple like a greeter module, that simply
greets users. A module can also be composed of other modules through
dependencies. For example, a music streaming module, may be composed of a
playlist/queue module, a voice chat module, and a music downloading/caching
module. This music stream module would be the module that controls them._


### Architecture
_The main run-time data store will be a Redux store._
