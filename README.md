# ImGui for Shaiya
ImGui page has a lot of info : https://github.com/ocornut/imgui

As a start I used the project Kiero : https://github.com/rdbo/ImGui-DirectX-9-Kiero-Hook

# Notes

       {
            static float f = 0.0f;
            static int counter = 0;

            ImGuiWindowFlags window_flags = 0;
            //window_flags |= ImGuiWindowFlags_NoBackground;
            window_flags |= ImGuiWindowFlags_NoCollapse; 
            window_flags |= ImGuiWindowFlags_NoMove; 
            bool open_ptr = true;

            ImGui::SetNextWindowContentSize(ImVec2(200, 200));
            ImGui::SetNextWindowSize(ImVec2(400, 400));
            ImGui::PushStyleVar(ImGuiStyleVar_WindowPadding, ImVec2(0, 0));
            
            ImGui::Begin("I'm a Window!", &open_ptr, window_flags | ImGuiWindowFlags_AlwaysAutoResize);
            ImVec2 p1 = ImGui::GetCursorScreenPos();
            ImVec2 p2 = ImVec2(p1.x + 200, p1.y + 200);


            if (ImGui::Button("Button")) // Buttons return true when clicked (most widgets return true when edited/activated)
                counter++;
            ImGui::SameLine();
            ImGui::Text("counter = %d", counter);

            ImGui::SetCursorPos(ImVec2(45, 380)); // Next frame position
            ImGui::Text("Application average %.3f ms/frame (%.1f FPS)", 1000.0f / ImGui::GetIO().Framerate, ImGui::GetIO().Framerate);
            ImGui::End();
            ImGui::PopStyleVar();
        }
        
        
![Ekran Alıntısı](https://user-images.githubusercontent.com/50587074/97797058-524a5100-1c22-11eb-8244-4860c4e15d57.PNG)

            

