# Copyright 2025 The Kubernetes Authors.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.


FROM python:3-alpine

ARG USER=1001

WORKDIR /docs
COPY docs /docs
COPY tools/docs/requirements.txt /docs  

RUN adduser -h /docs -D -u $USER mkdocs \
&& apk add bash \
&& apk add git 

RUN ls -la 
RUN ls -la /docs

RUN pip install --upgrade pip
RUN pip install -r /docs/requirements.txt