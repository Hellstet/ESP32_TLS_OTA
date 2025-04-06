idf_component_register(SRCS "hello_world_main.c"  # Or your actual main C file name
                    INCLUDE_DIRS "."            # Standard practice to include the current directory
                    REQUIRES nvs_flash
                             spi_flash           # Required for saving Wi-Fi credentials & general init
                             esp_netif           # Required for network interface abstraction (TCP/IP)
                             esp_event           # Required for handling system events (like Wi-Fi connect/disconnect)
                             esp_wifi            # Required for Wi-Fi functions (connect, etc.)
                             esp_http_client     # Required for making HTTP requests (to check version.txt)
                             esp_https_ota       # Required for the OTA update process itself
                             app_update      # Provides OTA data structures and functions like esp_ota_get_app_description
                             esp-tls             # Required by esp_https_ota, even for HTTP connections (it handles the abstraction)
                             log                 # Required for using ESP_LOGI, ESP_LOGE etc. (good practice)
                   )