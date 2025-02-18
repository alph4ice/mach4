# What is Mach4
Mach4 is a Python3 framework allowing the creation of APIs in a simple, fast and secure way, by managing Json Web Token signature.
# Why use an API framework
Mach4 provides the developer with a security system that allows the developer to develop its APIs while guaranteeing the authentication of its end users.
# Concrete case study
A developer wants to create a service. This service requires the use of an API to allow each user's information to be stored. But the developer wants a user to have access only to his information, of course. To do this, he could create an API in Python with Flask or Django, create a reliable authentication system meeting the latest security standards using Json Web Token, add a double security system to prevent the exploitation of XSS and CRSF vulnerabilities, manage the expiration of digital signature keys, allow the verification of his digital signatures... or simply design his API using Mach4, without worrying about its security.
# Why Mach4 and not another
Unlike other API frameworks such as Amazon API Gateway, Mach4 is not proprietary. Mach4 is available under the Apache 2.0 license, which guarantees complete transparency, so you can be sure that GAFAM will not use your users' personal data. Nor are you limited to a cloud platform. Mach4 being Open Source, you can use it on any platform you wish, or even develop your own.
# How to use Mach4
## 1. Install
```bash
python3 -m pip install mach4 
```
## 2. Import
```python
import mach4 
```
## 3. Initialise
```python
api = mach4.API("My API Name", "1.0", __name__)
```
## 4. Add
```python
def index():
	return "You’re logged!"
api.add_route("/index", accept_method = ["GET", "POST"], auth_required = True)
```
# Documentation
Refer to in-code comments.
# License
   Copyright 2021 Cyriaque Perier

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.