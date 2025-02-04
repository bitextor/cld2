cmake_minimum_required(VERSION 3.10)

project(cld2)

set(CMAKE_CXX_FLAGS "-Wno-narrowing -O3")

add_library(cld2_full SHARED 
    ${PROJECT_SOURCE_DIR}/internal/cldutil.cc
    ${PROJECT_SOURCE_DIR}/internal/cldutil_shared.cc
    ${PROJECT_SOURCE_DIR}/internal/compact_lang_det.cc
    ${PROJECT_SOURCE_DIR}/internal/compact_lang_det_hint_code.cc
    ${PROJECT_SOURCE_DIR}/internal/compact_lang_det_impl.cc
    ${PROJECT_SOURCE_DIR}/internal/debug.cc
    ${PROJECT_SOURCE_DIR}/internal/fixunicodevalue.cc
    ${PROJECT_SOURCE_DIR}/internal/generated_entities.cc
    ${PROJECT_SOURCE_DIR}/internal/generated_language.cc
    ${PROJECT_SOURCE_DIR}/internal/generated_ulscript.cc
    ${PROJECT_SOURCE_DIR}/internal/getonescriptspan.cc
    ${PROJECT_SOURCE_DIR}/internal/lang_script.cc
    ${PROJECT_SOURCE_DIR}/internal/offsetmap.cc
    ${PROJECT_SOURCE_DIR}/internal/scoreonescriptspan.cc
    ${PROJECT_SOURCE_DIR}/internal/tote.cc
    ${PROJECT_SOURCE_DIR}/internal/utf8statetable.cc
    ${PROJECT_SOURCE_DIR}/internal/cld_generated_cjk_uni_prop_80.cc
    ${PROJECT_SOURCE_DIR}/internal/cld2_generated_cjk_compatible.cc
    ${PROJECT_SOURCE_DIR}/internal/cld_generated_cjk_delta_bi_32.cc
    ${PROJECT_SOURCE_DIR}/internal/generated_distinct_bi_0.cc
    ${PROJECT_SOURCE_DIR}/internal/cld2_generated_quad0122.cc
    ${PROJECT_SOURCE_DIR}/internal/cld2_generated_deltaocta0122.cc
    ${PROJECT_SOURCE_DIR}/internal/cld2_generated_distinctocta0122.cc
    ${PROJECT_SOURCE_DIR}/internal/cld_generated_score_quad_octa_0122.cc
    )

set_target_properties(cld2_full PROPERTIES PUBLIC_HEADER ${PROJECT_SOURCE_DIR}/public/compact_lang_det.h)
