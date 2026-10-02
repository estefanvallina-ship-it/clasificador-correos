import streamlit as st

st.set_page_config(page_title="Clasificador de Correos", page_icon="📬")

st.title("📬 Mi Clasificador de Correos Inteligente")
st.write("Escribe el asunto de tu correo para saber su nivel de prioridad:")

# Caja de texto interactiva
asunto_correo = st.text_input("Asunto del correo:")

if asunto_correo:
    # Lógica de clasificación
    asunto_minusculas = asunto_correo.lower()
    
    urgentes = ["urgente", "emergencia", "asap", "inmediato", "caído", "error crítico"]
    moderados = ["importante", "factura", "revisar", "pendiente", "reunión"]
    
    if any(p in asunto_minusculas for p in urgentes):
        st.error("🚨 [PRIORIDAD ALTA] ¡Correo URGENTE! Atender de inmediato.")
    elif any(p in asunto_minusculas for p in moderados):
        st.warning("⚠️ [PRIORIDAD MEDIA] Correo IMPORTANTE. Revisar hoy.")
    else:
        st.success("✅ [PRIORIDAD BAJA] Correo normal. Sin prisa.")
