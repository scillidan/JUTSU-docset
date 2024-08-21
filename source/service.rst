Service
=======

.. option:: Jellyfin

	``mprocs "jellyfin.exe --service" "timeout 20 && .../jellyfin-mpv-shim/current/run.exe"``

.. option:: Komga

	``java.exe -jar "komga.jar" --komga.config-dir=".../config" %*``

.. option:: Datasette

	``datasette database.db --metadata metadata.json --root``

.. option:: bukuserver

	``bukuserver run --host 127.0.0.1 --port 5001``

.. option:: etherpad

	``cd D:\srv\etherpad-lite && start.bat``

.. option:: sqlite-web

	``sqlite_web -p 8050 $1 bookmarks.db``

.. option:: rclone-webui-angular

	``rclone rcd --rc-web-gui --rc-web-gui-update --rc-web-fetch-url="https://s3.yuudi.dev/rwa/embed/version.json"``

.. option:: calibre-web

	``calibre-server.exe --port 8084 .../calibre_dir``

.. option:: Logisim-evolution

	``javaw.exe -jar logisim-evolution.jar``

.. option:: pylanguagetool

	``echo-cli $* | pylanguagetool --api-url http://localhost:8081/v2/ --input-type txt --no-color --lang en-US``

.. option:: LanguageTool

	``java.exe -cp languagetool-server.jar org.languagetool.server.HTTPServer --port 8040 --allow-origin``

.. option:: Stable Diffusion web UI

	``open-cli http://127.0.0.1:7850/?__theme=dark && cd C:\Users\User\Github\AI-demo\stable-diffusion-webui && webui-user.bat``

.. option:: Faster Whisper Webui

	``open-cli http://127.0.0.1:7830 && cd C:\Users\User\Github\AI-demo\faster-whisper-webui && venv\Scripts\python.exe app.py --server_name 127.0.0.1 --server_port 7830 --input_audio_max_duration -1 --whisper_implementation "faster-whisper" --default_model_name "large-v2" --vad_parallel_devices "0" --auto_parallel true --output_dir "C:\Users\User\Downloads"``

.. option:: Backup Directory Opus

	``"C:\Users\User\Bin\trashy\trash.exe" "C:\Users\User\Data\directory-opus\backup*" && "C:\Program Files\GPSoftware\Directory Opus\dopusrt.exe" /cmd Prefs BACKUP=all TO "C:\Users\User\Data\directory-opus\backup_{date|yyyy-MM-dd}_{time|HH-mm-ss}" QUIET``

.. option:: Miniflux (Windows 10)

	``mprocs "gsudo postgres.exe -D miniflux_db" "timeout 5 && miniflux.exe -config-file miniflux.conf"``

.. option:: Linkding (Windows 10)

	``cd linkding && set LD_SUPERUSER_NAME=YourName && set LD_SUPERUSER_PASSWORD=YourPassword && mprocs "npm run dev" "timeout 5 && .\venv\Scripts\python.exe manage.py runserver 8002"``