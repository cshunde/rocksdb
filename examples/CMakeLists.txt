set(EXAMPLES
        simple_example.cc
        column_families_example.cc
        compact_files_example.cc
        compaction_filter_example.cc
        optimistic_transaction_example.cc
        options_file_example.cc
        transaction_example.cc)
foreach(src ${EXAMPLES})
    get_filename_component(exename ${src} NAME_WE)
    add_executable(${exename}${ARTIFACT_SUFFIX}
            ${src})
    target_link_libraries(${exename}${ARTIFACT_SUFFIX} ${LIBS})
endforeach()

