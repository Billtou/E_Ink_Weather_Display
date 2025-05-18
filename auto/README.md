16MB 參數

      platformio_options:  # 優化記憶體與快取處理
        board_build.arduino.memory_type: qio_opi
        board_build.flash_mode: qio
        build_flags:
          - "-DCONFIG_SPIRAM_CACHE_WORKAROUND"
          - "-mfix-esp32-psram-cache-issue"
    
    esp32:
      board: esp32-s3-devkitc-1
      variant: esp32s3
      flash_size: 16MB
      framework:
        type: arduino
    
    psram:
      mode: octal
      speed: 80MHz
8MB
      
      esp32:
        board: esp32-s3-devkitc-1
        variant: esp32s3
        flash_size: 8MB
        framework:
          type: arduino
      
      psram:
        mode: quad
        speed: 80MHz  
        
