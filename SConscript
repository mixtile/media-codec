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

Import('env')

install_path = '#out/lib32'
env["LIBPATH"] = [
  "#out/lib32",
]

# cedar base libraries
cedar_base_script = '#sunxi-cedarx/SOURCE/base/SConscript'
cedar_base_files = SConscript(cedar_base_script, variant_dir="build/base")
env.Install(install_path, cedar_base_files)

cedar_common_script = '#sunxi-cedarx/SOURCE/common/SConscript'
cedar_common_files = SConscript(cedar_common_script, variant_dir="build/common")
env.Install(install_path, cedar_common_files)

cedar_omxil_script = '#sunxi-cedarx/SOURCE/omxil/SConscript'
cedar_omxil_files = SConscript(cedar_omxil_script, variant_dir="build/omxil")
env.Install(install_path, cedar_omxil_files)

cedar_vencoder_script = '#sunxi-cedarx/SOURCE/vencoder/SConscript'
cedar_vencoder_files = SConscript(cedar_vencoder_script, variant_dir="build/vencoder")
env.Install(install_path, cedar_vencoder_files)

cedar_vdecoder_script = '#sunxi-cedarx/SOURCE/vdecoder/SConscript'
cedar_vdecoder_files = SConscript(cedar_vdecoder_script, variant_dir="build/vdecoder")
env.Install(install_path, cedar_vdecoder_files)

# cedar plugins libraries
cedar_h264_decoder_script = '#sunxi-cedarx/SOURCE/plugin/vdecoder/h264/SConscript'
cedar_h264_decoder_files = SConscript(cedar_h264_decoder_script, variant_dir="build/h264")
env.Install(install_path, cedar_h264_decoder_files)

cedar_mjpeg_decoder_script = '#sunxi-cedarx/SOURCE/plugin/vdecoder/mjpeg/SConscript'
cedar_mjpeg_decoder_files = SConscript(cedar_mjpeg_decoder_script, variant_dir="build/mjpeg")
env.Install(install_path, cedar_mjpeg_decoder_files)

cedar_mpeg2_decoder_script = '#sunxi-cedarx/SOURCE/plugin/vdecoder/mpeg2/SConscript'
cedar_mpeg2_decoder_files = SConscript(cedar_mpeg2_decoder_script, variant_dir="build/mpeg2")
env.Install(install_path, cedar_mpeg2_decoder_files)

cedar_mpeg4_decoder_script = '#sunxi-cedarx/SOURCE/plugin/vdecoder/mpeg4/SConscript'
cedar_mpeg4_decoder_files = SConscript(cedar_mpeg4_decoder_script, variant_dir="build/mpeg4")
env.Install(install_path, cedar_mpeg4_decoder_files)

# cedar extra plugins
cedar_extra_plugins_files = [
    "#media-codec-lib/lib32/lgnueabihf/libcedar_plugin_vd_others.so",
    "#media-codec-lib/lib32/lgnueabihf/libcedar_plugin_venc.so",
]
env.Install(install_path, cedar_extra_plugins_files)

# cedar test
cedar_test_script = '#sunxi-cedarx/demo/vencoder/SConscript'
cedar_test_files = SConscript(cedar_test_script, variant_dir="build/test")
env.Install("#out/bin", cedar_test_files)

