import tkinter as tk
from tkinter import messagebox

# --- COLORS & FONTS (The "Style Sheet") ---
BG_COLOR = "#2c3e50"     # Dark Blue-Grey (Background)
TEXT_COLOR = "#ecf0f1"   # Off-white (Text)
ACCENT_COLOR = "#e74c3c" # Red/Orange (Button)
BOX_COLOR = "#34495e"    # Lighter Grey (Input boxes/Results)
FONT_MAIN = ("Helvetica", 12)
FONT_BOLD = ("Helvetica", 12, "bold")

def calculate_time():
    try:
        dist_text = entry_distance.get()
        vehicle_type = vehicle_var.get()
        distance = float(dist_text)
        
        # Logic
        if vehicle_type == "Bike": speed = 40
        elif vehicle_type == "Car": speed = 60
        elif vehicle_type == "Drone": speed = 100
        else: speed = 40
            
        travel_mins = (distance / speed) * 60
        buffer_mins = 15 
        total_mins = travel_mins + buffer_mins
        
        # Fancy Result Text
        result_text = (
            f"🚀 Travel:   {travel_mins:.0f} min\n"
            f"📦 Handover: {buffer_mins} min\n"
            f"----------------------\n"
            f"⏱️ TOTAL:    {total_mins:.0f} min"
        )
        
        result_label.config(text=result_text, fg="#2ecc71") # Bright Green for success
        
    except ValueError:
        messagebox.showerror("Error", "Please enter a valid number.")

# --- GUI SETUP ---
root = tk.Tk()
root.title("Speed Logistics") # cooler name
root.geometry("400x500")
root.configure(bg=BG_COLOR) # Set main background color

# 1. Title Header
header_frame = tk.Frame(root, bg=BOX_COLOR, pady=20)
header_frame.pack(fill="x") # Fill the top width

tk.Label(header_frame, text="⚡ DELIVERY SYSTEM", font=("Arial", 16, "bold"), 
         bg=BOX_COLOR, fg=TEXT_COLOR).pack()

# 2. Main Content Area
content_frame = tk.Frame(root, bg=BG_COLOR, padx=20, pady=20)
content_frame.pack()

# Distance Input
tk.Label(content_frame, text="Destination Distance (km):", 
         font=FONT_MAIN, bg=BG_COLOR, fg=TEXT_COLOR).pack(anchor="w")

entry_distance = tk.Entry(content_frame, font=FONT_MAIN, bg=BOX_COLOR, 
                          fg="white", insertbackground="white") # 'insertbackground' changes cursor color
entry_distance.pack(fill="x", pady=5)

# Vehicle Input
tk.Label(content_frame, text="Select Vehicle:", 
         font=FONT_MAIN, bg=BG_COLOR, fg=TEXT_COLOR).pack(anchor="w", pady=(15,0))

vehicle_options = ["Bike", "Car", "Drone"]
vehicle_var = tk.StringVar(root)
vehicle_var.set("Bike")

# Styling the dropdown is tricky in Tkinter, so we keep it simple or use a specific config
dropdown = tk.OptionMenu(content_frame, vehicle_var, *vehicle_options)
dropdown.config(bg=BOX_COLOR, fg="white", activebackground=ACCENT_COLOR, highlightthickness=0)
dropdown["menu"].config(bg=BOX_COLOR, fg="white") # Style the popup list
dropdown.pack(fill="x", pady=5)

# 3. Big Action Button
btn_calc = tk.Button(root, text="CALCULATE ESTIMATE", font=FONT_BOLD, 
                     bg=ACCENT_COLOR, fg="white", activebackground="#c0392b", 
                     relief="flat", cursor="hand2", command=calculate_time)
btn_calc.pack(pady=20, ipadx=10, ipady=5) # ipad adds internal padding (makes button fatter)

# 4. Result Display (A "Card" look)
result_frame = tk.Frame(root, bg=BOX_COLOR, bd=2, relief="groove")
result_frame.pack(fill="x", padx=20, pady=10)

result_label = tk.Label(result_frame, text="Ready to calculate...", 
                        font=("Courier", 12), bg=BOX_COLOR, fg="#95a5a6", justify="left")
result_label.pack(pady=15)

root.mainloop()
