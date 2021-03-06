# About
Integration of Amplience Dynamic Content into SAP CX (Hybris).

Goal of this project is to provide a simple and flexible way to retrieve and integrate content into SAP CX (Hybris/Commerce).
This is done without too much assumptions on how the existing SAP CX System is constructed. 
The project is kind of a basis to build exactly what you need, not a one click solution.

The main idea of the integraiton is to trigger SAP CX via webhooks at the moment of creation or changes on slots.
Then all available information is downloaded from the Amplience virtual staging environment,
including the Slots JSON and prerendered HTML (from the content rendering service). Since all internal
IDs are preserved, the user can build integrations that:
* include prerendered HTML in a serverside rendered frontent (like JSPs)
* output cached JSON in an own API
* use the ID to lookup content in Amplience themself

The integration is capable of handling multiple localized websites/storefronts and even multiple Amplience
content hubs.

As there are only few dependencies on existing structures and data models in SAP CX, it should fit nearly 
for all project setups.

This integration provides different components:
* Hybris Extension `amplienceintegration` which provides webhook endpoints for events from Amplience
* Hybris Addon `amplienceaddon` that provides a Taglib to include Amplience content in the SAP CX templates
* Amplience JSON Schemas for Content Items and Slots

Please see the [documentation](docs/README.md) for more information.


# License
Copyright (c) 2020. neteleven GmbH (https://www.neteleven.de/)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
