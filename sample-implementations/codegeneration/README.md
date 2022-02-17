Sample project to see how code genaration could work. Also used to validate if the openapi definitions actually generate usefuill code

This uses gradlew, genarates java or php. More languages can be added easyly.
the used generator is : https://github.com/OpenAPITools/openapi-generator

> gradlew generatejava 
generated java implementation for each API. gerenator properties can be found in gradle.build

> gradlew generatephp 
generated php implementation for each API. gerenator properties can be found in gradle.build

