# Copyright (C) 2023 Intel Corporation
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions
# and limitations under the License.
#
# SPDX-License-Identifier: Apache-2.0

custom_target('docker-jstest',
  input : [files('Dockerfile.m4')],
  depend_files : [m4_templates],
  output : 'Dockerfile',
  command : [m4, m4_args,
    '-D', 'OS_NAME=ubuntu', '-D', 'OS_VERSION=22.04', '@INPUT@'],
  capture : true,
  install : true,
  install_dir : meson.current_source_dir(),
  )

