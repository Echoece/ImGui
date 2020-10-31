# ImGui for Shaiya
ImGui page has a lot of info : https://github.com/ocornut/imgui

As a start I used the project Kiero : https://github.com/rdbo/ImGui-DirectX-9-Kiero-Hook

# Notes
            ImGuiWindowFlags window_flags = 0;
            window_flags |= ImGuiWindowFlags_NoBackground;
            window_flags |= ImGuiWindowFlags_NoTitleBar;
            bool open_ptr = true;
            ImGui::Begin("I'm a Window!", &open_ptr, window_flags);


