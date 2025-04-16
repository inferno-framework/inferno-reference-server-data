# inferno-reference-server-data
This is the default data repository for the [Inferno US Core R4 Reference Server](https://github.com/inferno-framework/inferno-reference-server). Unless otherwise specified, an instance of the server will fetch this repository at first startup and load the resources it contains. 

## Running

This repository contains a docker-compose file for convenience, to make it easier for test kit developers to make data changes. To run an instance of the Inferno Reference Server, preloaded with the data in `./resources` and the custom clients under `./clients` : 

```
docker compose up
```

The server will be available at [http://localhost:8080/reference-server](http://localhost:8080/reference-server), and the FHIR endpoint is at
[http://localhost:8080/reference-server/r4](http://localhost:8080/reference-server/r4)

By default, the postgres database included here is not persisted with a volume, so restarting the containers will reload the latest contents of `./resources/`

## License

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0
Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

## Trademark Notice

HL7, FHIR and the FHIR [FLAME DESIGN] are the registered trademarks of Health
Level Seven International and their use does not constitute endorsement by HL7.
