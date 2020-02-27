<!--
#
# Licensed to the Apache Software Foundation (ASF) under one or more
# contributor license agreements.  See the NOTICE file distributed with
# this work for additional information regarding copyright ownership.
# The ASF licenses this file to You under the Apache License, Version 2.0
# (the "License"); you may not use this file except in compliance with
# the License.  You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
-->

# The new scheduling component.

## Status
* Current state: In-progress
* Author(s): @style95, @ningyougang  @jiangpengcheng @Keonhee @upgle

## Summary and Motivation

We propose a new component which is in charge of scheduling containers.  
This is a new standalone component which is comparable to controllers or invokers.
The component will decide how many containers need to be created and when to create them.

Our proposal is based on the observation that container operation can be much slower than execution time 
and because of the sequential nature in which Docker engine processes operations, it enormously degrades the performance of the system.  
Also, invokers can run codes directly when warmed containers are reused, so we can significantly improve the performance by maximizing container reuse.

The new component schedule containers taking into account these factors.


This section summarize the proposal.
A brief description, proposed changes, and effects are expected to be included.
You should cover the "what" and the "why" and briefly the "how".

## Proposed changes: Architecture Diagram (optional), and Design

This section may include large subsections, diagrams, links to references, and so on.

It is recommended to include an architectural diagram.
A link to an external resource is enough.

### Implementation details

This section describe how to implement the proposal.

## Issue (optional)

Any issue(compatibility, drawbacks, etc) should be describe here.

## Integration and Migration plan (optional)

If a proposal contains any breaking changes, it is required to include a plan for integration and migration.
