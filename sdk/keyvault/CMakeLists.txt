# Copyright (c) Microsoft Corporation.
# Licensed under the MIT License.

cmake_minimum_required (VERSION 3.13)

project (azure-security-keyvault LANGUAGES CXX)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

if(BUILD_TESTING)
  # define a symbol that enables some test hooks in code
  add_compile_definitions(_azure_TESTING_BUILD)
endif()

add_subdirectory(azure-security-keyvault-keys)
add_subdirectory(azure-security-keyvault-secrets)
add_subdirectory(azure-security-keyvault-certificates)
add_subdirectory(azure-security-keyvault-administration)
