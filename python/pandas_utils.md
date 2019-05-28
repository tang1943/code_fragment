```{.python .input}
import pandas as pd
def save_csv_to_excel(file_path, sheet_names, data_frames):
    writer = pd.ExcelWriter(file_path, engine='xlsxwriter')
    for sheet_name, df in zip(sheet_names, data_frames):
        df.to_excel(writer, sheet_name=sheet_name)
    writer.save()
```
