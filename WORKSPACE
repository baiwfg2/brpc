# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
# KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.

workspace(name = "com_github_brpc_brpc")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

skylib_version = "0.8.0"
http_archive(
    name = "bazel_skylib",
    type = "tar.gz",
    url = "https://github.com/bazelbuild/bazel-skylib/releases/download/{}/bazel-skylib.{}.tar.gz".format (skylib_version, skylib_version),
    sha256 = "2ef429f5d7ce7111263289644d233707dba35e39696377ebab8b0bc701f7818e",
)

http_archive(
  name = "com_google_protobuf",
  strip_prefix = "protobuf-3.6.1.3",
  sha256 = "9510dd2afc29e7245e9e884336f848c8a6600a14ae726adb6befdb4f786f0be2",
  type = "zip",
  url = "https://github.com/protocolbuffers/protobuf/archive/v3.6.1.3.zip",
)
  
http_archive(
    name = "com_github_gflags_gflags",
    strip_prefix = "gflags-46f73f88b18aee341538c0dfc22b1710a6abedef",
    url = "https://github.com/gflags/gflags/archive/46f73f88b18aee341538c0dfc22b1710a6abedef.tar.gz",
)
 
bind(
    name = "gflags",
    actual = "@com_github_gflags_gflags//:gflags",
)
  
http_archive(
    name = "com_github_google_leveldb",
    build_file = "//:leveldb.BUILD",
    strip_prefix = "leveldb-a53934a3ae1244679f812d998a4f16f2c7f309a6",
    url = "https://github.com/google/leveldb/archive/a53934a3ae1244679f812d998a4f16f2c7f309a6.tar.gz"
)

http_archive(
    name = "com_github_google_glog",
    build_file = "//:glog.BUILD",
    strip_prefix = "glog-a6a166db069520dbbd653c97c2e5b12e08a8bb26",
    url = "https://github.com/google/glog/archive/a6a166db069520dbbd653c97c2e5b12e08a8bb26.tar.gz"
)
  
http_archive(
    name = "com_google_googletest",
    strip_prefix = "googletest-0fe96607d85cf3a25ac40da369db62bbee2939a5",
    url = "https://github.com/google/googletest/archive/0fe96607d85cf3a25ac40da369db62bbee2939a5.tar.gz",
)

http_archive(
    name = "com_google_tcmalloc",
    urls = ["https://github.com/google/tcmalloc/archive/9c5390e25c8612332251983d30ca6501bce9d41f.zip"],
    strip_prefix = "tcmalloc-9c5390e25c8612332251983d30ca6501bce9d41f",
    sha256 = "dd1e3f8b8c83c61cd13deea53832f985adb29e0093159539995d72cf989bf258",
)

# tcmalloc依赖于它
http_archive(
    name = "com_google_absl",
    urls = ["https://github.com/abseil/abseil-cpp/archive/a1d6689907864974118e592ef2ac7d716c576aad.zip"],
    strip_prefix = "abseil-cpp-a1d6689907864974118e592ef2ac7d716c576aad",
    sha256 = "53b78ffe87db3c737feddda52fa10dcdb75e2d85eed1cb1c5bfd77ca22e53e53",
)