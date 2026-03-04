** start of main.py **

test_settings = {'Scocco':'Delantero/Extremo', 'Heinze':'Defensor Central', 'Rodriguez':'Mediocampista/Delantero'}
cuple = ('THEME', 'Oceanic')

def add_setting(diccionario, tupla):
    new_key = tupla[0].lower()
    new_val = tupla[1].lower()

    if new_key in diccionario:
        return f"Setting '{new_key}' already exists! Cannot add a new setting with this name."
    else:
        diccionario[new_key] = new_val
        return f"Setting '{new_key}' added with value '{new_val}' successfully!"

def update_setting(uno, dos):
    upd_key = dos[0].lower()
    upd_val = dos[1].lower()

    if upd_key in uno:
        uno.update({upd_key:upd_val})
        return f"Setting '{upd_key}' updated to '{upd_val}' successfully!"
    
    return f"Setting '{upd_key}' does not exist! Cannot update a non-existing setting."

def delete_setting(dicc3, llave):
    del_key = llave.lower()

    if del_key in dicc3:
        dicc3.pop(del_key)
        return f"Setting '{del_key}' deleted successfully!"
    
    return f"Setting not found!"

def view_settings(settings):
    if settings == {}:
        return "No settings available."
    output = "Current User Settings:\n"
    for key, value in settings.items():
        output += f"{key.capitalize()}: {value}\n"
    return output

print(view_settings(test_settings))      

** end of main.py **

