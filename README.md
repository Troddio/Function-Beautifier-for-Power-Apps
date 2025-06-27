# Function-Beautifier-for-Power-Apps
Funzione per formattare le espressioni PowerApps in modo leggibile. Questa funzione indentifica le funzioni inline e gestisce le parentesi e le virgole per migliorare la leggibilità.

Funzione per formattare le espressioni PowerApps in modo leggibile.
Questa funzione indentifica le funzioni inline e gestisce le parentesi e le virgole, mantenendo su una linea i contenuti delle di "body(...)", "coalesce(...)", "outputs(...)" e "output(...)"
@param {string} expr - L'espressione PowerApps da formattare.
@return {string} - L'espressione formattata.

@example
Input = "if(equals(add(coalesce(first(outputs('Elenca_righe:_Calcoli')?['body/value'])?['something_1'],0),coalesce(first(outputs('Elenca_righe:_Calcoli')?['body/value'])?['something_2'],0)),0,div(body('Analizza_JSON')?['something_3'],add(coalesce(first(outputs('Elenca_righe:_Calcoli')?['body/value'])?['something_1'],0),coalesce(first(outputs('Elenca_righe:_Calcoli')?['body/value'])?['something_2'],0))))";

Output:
if(
    equals(
         add(
            coalesce(first(outputs('Elenca_righe:_Calcoli')?['body/value'])?['something_1'],0),
            coalesce(first(outputs('Elenca_righe:_Calcoli')?['body/value'])?['something_2'],0)
        ),
        0,
        div(
            body('Analizza_JSON')?['something_3'],
            add(
                coalesce(first(outputs('Elenca_righe:_Calcoli')?['body/value'])?['something_1'],0),
                coalesce(first(outputs('Elenca_righe:_Calcoli')?['body/value'])?['something_2'],0)
            )
        )
)
