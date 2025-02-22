cmake_minimum_required(VERSION 3.15)
project(websocketpp)

set(CMAKE_CXX_STANDARD 14)

include_directories(examples/echo_server)
include_directories(examples/external_io_service)
include_directories(test/connection)
include_directories(websocketpp)
include_directories(websocketpp/base64)
include_directories(websocketpp/common)
include_directories(websocketpp/concurrency)
include_directories(websocketpp/config)
include_directories(websocketpp/extensions)
include_directories(websocketpp/extensions/permessage_deflate)
include_directories(websocketpp/http)
include_directories(websocketpp/http/impl)
include_directories(websocketpp/impl)
include_directories(websocketpp/logger)
include_directories(websocketpp/message_buffer)
include_directories(websocketpp/processors)
include_directories(websocketpp/random)
include_directories(websocketpp/roles)
include_directories(websocketpp/sha1)
include_directories(websocketpp/transport)
include_directories(websocketpp/transport/asio)
include_directories(websocketpp/transport/asio/security)
include_directories(websocketpp/transport/base)
include_directories(websocketpp/transport/debug)
include_directories(websocketpp/transport/iostream)
include_directories(websocketpp/transport/stub)

add_executable(websocketpp
        docs/simple_broadcast_server.cpp
        docs/simple_count_server_thread.cpp
        examples/associative_storage/associative_storage.cpp
        examples/broadcast_server/broadcast_server.cpp
        examples/debug_client/debug_client.cpp
        examples/debug_server/debug_server.cpp
        examples/dev/main.cpp
        examples/echo_client/echo_client.cpp
        examples/echo_server/echo_handler.hpp
        examples/echo_server/echo_server.cpp
        examples/echo_server_both/echo_server_both.cpp
        examples/echo_server_tls/echo_server_tls.cpp
        examples/enriched_storage/enriched_storage.cpp
        examples/external_io_service/external_io_service.cpp
        examples/external_io_service/tcp_echo_server.hpp
        examples/handler_switch/handler_switch.cpp
        examples/iostream_server/iostream_server.cpp
        examples/print_client/print_client.cpp
        examples/print_client_tls/print_client_tls.cpp
        examples/print_server/print_server.cpp
        examples/scratch_client/scratch_client.cpp
        examples/scratch_server/scratch_server.cpp
        examples/simple_broadcast_server/simple_broadcast_server.cpp
        examples/sip_client/sip_client.cpp
        examples/subprotocol_server/subprotocol_server.cpp
        examples/telemetry_client/telemetry_client.cpp
        examples/telemetry_server/telemetry_server.cpp
        examples/testee_client/testee_client.cpp
        examples/testee_server/testee_server.cpp
        examples/utility_client/utility_client.cpp
        test/connection/connection.cpp
        test/connection/connection_tu2.cpp
        test/connection/connection_tu2.hpp
        test/endpoint/endpoint.cpp
        test/extension/extension.cpp
        test/extension/permessage_deflate.cpp
        test/http/parser.cpp
        test/http/parser_perf.cpp
        test/logger/basic.cpp
        test/message_buffer/alloc.cpp
        test/message_buffer/message.cpp
        test/message_buffer/pool.cpp
        test/processors/extension_permessage_compress.cpp
        test/processors/hybi00.cpp
        test/processors/hybi07.cpp
        test/processors/hybi08.cpp
        test/processors/hybi13.cpp
        test/processors/processor.cpp
        test/random/none.cpp
        test/random/random_device.cpp
        test/roles/client.cpp
        test/roles/server.cpp
        test/transport/asio/base.cpp
        test/transport/asio/security.cpp
        test/transport/asio/timers.cpp
        test/transport/iostream/base.cpp
        test/transport/iostream/connection.cpp
        test/transport/iostream/endpoint.cpp
        test/transport/hybi_util.cpp
        test/transport/integration.cpp
        test/utility/close.cpp
        test/utility/error.cpp
        test/utility/frame.cpp
        test/utility/sha1.cpp
        test/utility/uri.cpp
        test/utility/utilities.cpp
        tutorials/utility_client/step1.cpp
        tutorials/utility_client/step2.cpp
        tutorials/utility_client/step3.cpp
        tutorials/utility_client/step4.cpp
        tutorials/utility_client/step5.cpp
        tutorials/utility_client/step6.cpp
        tutorials/utility_server/step1.cpp
        tutorials/utility_server/step2.cpp
        websocketpp/base64/base64.hpp
        websocketpp/common/asio.hpp
        websocketpp/common/asio_ssl.hpp
        websocketpp/common/chrono.hpp
        websocketpp/common/connection_hdl.hpp
        websocketpp/common/cpp11.hpp
        websocketpp/common/functional.hpp
        websocketpp/common/md5.hpp
        websocketpp/common/memory.hpp
        websocketpp/common/network.hpp
        websocketpp/common/platforms.hpp
        websocketpp/common/random.hpp
        websocketpp/common/regex.hpp
        websocketpp/common/stdint.hpp
        websocketpp/common/system_error.hpp
        websocketpp/common/thread.hpp
        websocketpp/common/time.hpp
        websocketpp/common/type_traits.hpp
        websocketpp/concurrency/basic.hpp
        websocketpp/concurrency/none.hpp
        websocketpp/config/asio.hpp
        websocketpp/config/asio_client.hpp
        websocketpp/config/asio_no_tls.hpp
        websocketpp/config/asio_no_tls_client.hpp
        websocketpp/config/boost_config.hpp
        websocketpp/config/core.hpp
        websocketpp/config/core_client.hpp
        websocketpp/config/debug.hpp
        websocketpp/config/debug_asio.hpp
        websocketpp/config/debug_asio_no_tls.hpp
        websocketpp/config/minimal_client.hpp
        websocketpp/config/minimal_server.hpp
        websocketpp/extensions/permessage_deflate/disabled.hpp
        websocketpp/extensions/permessage_deflate/enabled.hpp
        websocketpp/extensions/extension.hpp
        websocketpp/http/impl/parser.hpp
        websocketpp/http/impl/request.hpp
        websocketpp/http/impl/response.hpp
        websocketpp/http/constants.hpp
        websocketpp/http/parser.hpp
        websocketpp/http/request.hpp
        websocketpp/http/response.hpp
        websocketpp/impl/connection_impl.hpp
        websocketpp/impl/endpoint_impl.hpp
        websocketpp/impl/utilities_impl.hpp
        websocketpp/logger/basic.hpp
        websocketpp/logger/levels.hpp
        websocketpp/logger/stub.hpp
        websocketpp/logger/syslog.hpp
        websocketpp/message_buffer/alloc.hpp
        websocketpp/message_buffer/message.hpp
        websocketpp/message_buffer/pool.hpp
        websocketpp/processors/base.hpp
        websocketpp/processors/hybi00.hpp
        websocketpp/processors/hybi07.hpp
        websocketpp/processors/hybi08.hpp
        websocketpp/processors/hybi13.hpp
        websocketpp/processors/processor.hpp
        websocketpp/random/none.hpp
        websocketpp/random/random_device.hpp
        websocketpp/roles/client_endpoint.hpp
        websocketpp/roles/server_endpoint.hpp
        websocketpp/sha1/sha1.hpp
        websocketpp/transport/asio/security/base.hpp
        websocketpp/transport/asio/security/none.hpp
        websocketpp/transport/asio/security/tls.hpp
        websocketpp/transport/asio/base.hpp
        websocketpp/transport/asio/connection.hpp
        websocketpp/transport/asio/endpoint.hpp
        websocketpp/transport/base/connection.hpp
        websocketpp/transport/base/endpoint.hpp
        websocketpp/transport/debug/base.hpp
        websocketpp/transport/debug/connection.hpp
        websocketpp/transport/debug/endpoint.hpp
        websocketpp/transport/iostream/base.hpp
        websocketpp/transport/iostream/connection.hpp
        websocketpp/transport/iostream/endpoint.hpp
        websocketpp/transport/stub/base.hpp
        websocketpp/transport/stub/connection.hpp
        websocketpp/transport/stub/endpoint.hpp
        websocketpp/client.hpp
        websocketpp/close.hpp
        websocketpp/connection.hpp
        websocketpp/connection_base.hpp
        websocketpp/endpoint.hpp
        websocketpp/endpoint_base.hpp
        websocketpp/error.hpp
        websocketpp/frame.hpp
        websocketpp/server.hpp
        websocketpp/uri.hpp
        websocketpp/utf8_validator.hpp
        websocketpp/utilities.hpp
        websocketpp/version.hpp)
