
Tool Name: create_lead

Description: Creates a new lead record in the enrollment system with basic contact information. Returns a unique lead_id for subsequent updates.

Parameters:

first_name (string, required): Client's first name.

last_name (string, required): Client's last name.

phone_number (string, required): Client's contact phone number.

Tool Name: update_lead

Description: Updates the existing lead record with additional collected data. Accepts multiple fields simultaneously.

Parameters:

lead_id (string, required): The unique identifier for the lead record.

date_of_birth (string, optional): Client's date of birth (MM/DD/YYYY).

address (string, optional): Client's full street address, including city, state, and zip.

income_source (string, optional): Client's primary source of monthly income.

hardship_description (string, optional): Description of the client's financial hardship.

[corrected_field] (string, optional): Field name to correct during confirmation step.

[corrected_value] (string, optional): New value for the corrected field.

Tool Name: prequalify_client

Description: Submits the collected identity and financial data to the pre-qualification engine for a soft credit pull.

Parameters:

lead_id (string, required): The unique identifier for the lead record.

Returns: A boolean result indicating if the client is pre-qualified (True/False).

Tool Name: schedule_call

Description: Triggers the system to schedule a specialist call with the pre-qualified client at a later time.

Parameters:

lead_id (string, required): The unique identifier for the lead record.

Tool Name: transfer_to_agent

Description: Transfers the live chat session to a human sales agent immediately.

Parameters:

lead_id (string, required): The unique identifier for the lead record.