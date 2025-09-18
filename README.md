diff --git a//dev/null b/python/README.md
index 0000000000000000000000000000000000000000..13f87fa71ab73986a856dc6ea8a57d41fbc6c1d5 100644
--- a//dev/null
+++ b/python/README.md
@@ -0,0 +1,33 @@
+# Streamlit + Supabase chat demo
+
+This simple Streamlit application shows how to:
+
+1. Connect to Supabase using the REST API.
+2. Create a table named `chat_table` that stores `chat_id` and `chat_message`.
+3. Insert and display chat messages through the Supabase Python client.
+
+## Setup
+
+1. Install the Python dependencies:
+
+   ```bash
+   pip install -r python/requirements.txt
+   ```
+
+2. Export your Supabase credentials (optional, they can also be provided through the Streamlit UI):
+
+   ```bash
+   export SUPABASE_URL="https://your-project.supabase.co"
+   export SUPABASE_ANON_KEY="anon-public-api-key"
+   export SUPABASE_SERVICE_ROLE_KEY="service-role-key"
+   ```
+
+3. Start the Streamlit app:
+
+   ```bash
+   streamlit run python/streamlit_supabase_chat.py
+   ```
+
+4. Use the sidebar in the app to provide your Supabase URL and keys, then click **Initialize chat table** to create the `chat_table`. Afterwards you can send messages and view them in the UI.
+
+> **Security tip:** Only run the app in a secure environment when using the service role key because it has elevated privileges.
