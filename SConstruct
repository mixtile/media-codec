#
# Copyright (C) 2015 Focalcrest, Inc.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

import os

platform = ARGUMENTS.get('platform','arm')  


EXE_PATH = '../buildroot/output/host/usr/bin'
PREFIX = EXE_PATH+ '/arm-linux-gnueabihf-'

env = Environment()
    
env["CC"] = PREFIX + 'gcc'  
env["CXX"] = PREFIX + 'g++'    
env["AS"] = PREFIX + 'gcc'    
env["AR"] = PREFIX + 'ar'    
env["LINK"] = PREFIX + 'gcc' 
env["platform"] = platform

env.PrependENVPath ('PATH', EXE_PATH)

Export("env")

cedar_script = '#SConscript'
cedar_files = SConscript(cedar_script)

