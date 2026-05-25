# TFM
[Untitled14.ipynb](https://github.com/user-attachments/files/28230548/Untitled14.ipynb)
{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 12,
   "id": "86956cf1-d274-4cb4-8cc9-be0a8c3b63b6",
   "metadata": {},
   "outputs": [],
   "source": [
    "import yfinance as yf\n",
    "import pandas as pd"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "id": "766bb60b-5836-445a-bab3-04d434313645",
   "metadata": {},
   "outputs": [],
   "source": [
    "macys=yf.Ticker(\"M\")\n",
    "amazon=yf.Ticker(\"AMZN\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 14,
   "id": "1ca7b431-d82b-44e6-866c-c0d2373ce230",
   "metadata": {},
   "outputs": [],
   "source": [
    "df_macys=macys.financials\n",
    "df_amazon=amazon.financials"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "id": "17f028ac-1fc6-4c19-8eac-c7e5eb10f956",
   "metadata": {},
   "outputs": [
    {
     "ename": "SyntaxError",
     "evalue": "invalid syntax. Perhaps you forgot a comma? (3527616771.py, line 1)",
     "output_type": "error",
     "traceback": [
      "  \u001b[36mCell\u001b[39m\u001b[36m \u001b[39m\u001b[32mIn[15]\u001b[39m\u001b[32m, line 1\u001b[39m\n\u001b[31m    \u001b[39m\u001b[31mprint(\"ANALISI DE DATOS MACY'S\"\u001b[39m\n          ^\n\u001b[31mSyntaxError\u001b[39m\u001b[31m:\u001b[39m invalid syntax. Perhaps you forgot a comma?\n"
     ]
    }
   ],
   "source": [
    "print(\"ANALISI DE DATOS MACY'S\"\n",
    "print(\"KPI Macy's\"\n",
    "print(df_macys.index.tolist)))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "id": "9e4b067a-d5d4-406d-908d-856138ce3244",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "--- ANALISIs DATASET MACY'S ---\n",
      "Dimensiones de dataset Macy's (Rigas, Columnas): (49, 5)\n",
      "\n",
      "Balance (Rigas) de Macy's:\n",
      "['Tax Effect Of Unusual Items', 'Tax Rate For Calcs', 'Normalized EBITDA', 'Total Unusual Items', 'Total Unusual Items Excluding Goodwill', 'Net Income From Continuing Operation Net Minority Interest', 'Reconciled Depreciation', 'Reconciled Cost Of Revenue', 'EBITDA', 'EBIT', 'Net Interest Income', 'Interest Expense', 'Interest Income', 'Normalized Income', 'Net Income From Continuing And Discontinued Operation', 'Total Expenses', 'Total Operating Income As Reported', 'Diluted Average Shares', 'Basic Average Shares', 'Diluted EPS', 'Basic EPS', 'Diluted NI Availto Com Stockholders', 'Net Income Common Stockholders', 'Net Income', 'Net Income Including Noncontrolling Interests', 'Net Income Continuous Operations', 'Tax Provision', 'Pretax Income', 'Other Income Expense', 'Other Non Operating Income Expenses', 'Special Income Charges', 'Other Special Charges', 'Write Off', 'Restructuring And Mergern Acquisition', 'Gain On Sale Of Security', 'Net Non Operating Interest Income Expense', 'Total Other Finance Cost', 'Interest Expense Non Operating', 'Interest Income Non Operating', 'Operating Income', 'Operating Expense', 'Selling General And Administration', 'General And Administrative Expense', 'Other Gand A', 'Salaries And Wages', 'Gross Profit', 'Cost Of Revenue', 'Total Revenue', 'Operating Revenue']\n",
      "--------------------------------------------------\n",
      "\n",
      " ANALISIS DATASET AMAZON \n",
      "Dimensiones de dataset Amazon (Rigas, Columnas): (45, 4)\n",
      "\n",
      "Balance (Rigas) de Amazon:\n",
      "['Tax Effect Of Unusual Items', 'Tax Rate For Calcs', 'Normalized EBITDA', 'Total Unusual Items', 'Total Unusual Items Excluding Goodwill', 'Net Income From Continuing Operation Net Minority Interest', 'Reconciled Depreciation', 'Reconciled Cost Of Revenue', 'EBITDA', 'EBIT', 'Net Interest Income', 'Interest Expense', 'Interest Income', 'Normalized Income', 'Net Income From Continuing And Discontinued Operation', 'Total Expenses', 'Total Operating Income As Reported', 'Diluted Average Shares', 'Basic Average Shares', 'Diluted EPS', 'Basic EPS', 'Diluted NI Availto Com Stockholders', 'Net Income Common Stockholders', 'Net Income', 'Net Income Including Noncontrolling Interests', 'Net Income Continuous Operations', 'Earnings From Equity Interest Net Of Tax', 'Pretax Income', 'Other Income Expense', 'Other Non Operating Income Expenses', 'Gain On Sale Of Security', 'Net Non Operating Interest Income Expense', 'Interest Expense Non Operating', 'Interest Income Non Operating', 'Operating Income', 'Operating Expense', 'Other Operating Expenses', 'Selling General And Administration', 'Selling And Marketing Expense', 'General And Administrative Expense', 'Other Gand A', 'Gross Profit', 'Cost Of Revenue', 'Total Revenue', 'Operating Revenue']\n",
      "--------------------------------------------------\n"
     ]
    }
   ],
   "source": [
    "print(\"--- ANALISIs DATASET MACY'S ---\")\n",
    "\n",
    "print(f\"Dimensiones de dataset Macy's (Rigas, Columnas): {df_macys.shape}\\n\")\n",
    "\n",
    "\n",
    "print(\"Balance (Rigas) de Macy's:\")\n",
    "print(df_macys.index.tolist())\n",
    "print(\"-\" * 50)\n",
    "\n",
    "\n",
    "print(\"\\n ANALISIS DATASET AMAZON \")\n",
    "\n",
    "print(f\"Dimensiones de dataset Amazon (Rigas, Columnas): {df_amazon.shape}\\n\")\n",
    "\n",
    "\n",
    "print(\"Balance (Rigas) de Amazon:\")\n",
    "print(df_amazon.index.tolist())\n",
    "print(\"-\" * 50)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "9636d24e-7d72-4fcb-99f9-d8f9d5cd5028",
   "metadata": {},
   "outputs": [],
   "source": [
    "print(df_macys)\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "892fcf17-77c9-4d6f-86de-643d65250cdc",
   "metadata": {},
   "outputs": [],
   "source": [
    "print (df_amazon)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "e1990d54-addc-46cc-b29a-68f7be1a3ebd",
   "metadata": {},
   "outputs": [],
   "source": [
    "marks_spencer=yf.Ticker(\"MS\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "4553bec6-fb16-41b1-9ca2-5b46e9c6a606",
   "metadata": {},
   "outputs": [],
   "source": [
    "df_marks_spencer=marks_spencer.financials"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "17da059e-ccd7-4967-ad73-feb59cd2bdc8",
   "metadata": {},
   "outputs": [],
   "source": [
    "print (\"ANALISIS DATASET MARKS E SPENCER\")\n",
    "print(f\"Dimension dataset Marks Spencer (Righe, Colonne) : [df_marks_spencer.shape]\\n\")\n",
    "print(df_marks_spencer.index.tolist())\n",
    "print(\"-\"*50)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "919412a3-cbe3-473e-8f5b-ce0e8182fa5a",
   "metadata": {},
   "outputs": [],
   "source": [
    "print (df_marks_spencer)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "id": "2c0bd336-6ea4-4669-8dec-ea781a6e6751",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Descargar datos da Yahoo Finance...\n",
      "alineación independiente de las tablas se ha completado con éxito!\n",
      "\n",
      "--- DATASET COMPLETO PER IL TFM ---\n",
      "                 Total Revenue ($)  Gross Margin (%)  Cost of Revenue (%)  \\\n",
      "Amazon             716924000000.00             50.29                49.71   \n",
      "Macy's              22621000000.00             40.33                59.67   \n",
      "Marks & Spencer                NaN               NaN                  NaN   \n",
      "Coin                  169950000.00             43.50                56.50   \n",
      "El Corte Inglés     15800000000.00               NaN                  NaN   \n",
      "\n",
      "                 SG&A Margin (%)  Operating Margin (%)  EBITDA Margin (%)  \\\n",
      "Amazon                      8.13                 11.16              23.06   \n",
      "Macy's                     36.43                  3.91               8.13   \n",
      "Marks & Spencer              NaN                   NaN                NaN   \n",
      "Coin                         NaN                   NaN             -30.60   \n",
      "El Corte Inglés              NaN                   NaN               7.59   \n",
      "\n",
      "                 Inventory Turnover  Sales per Sq Ft  \n",
      "Amazon                         9.30              NaN  \n",
      "Macy's                         3.06           180.00  \n",
      "Marks & Spencer                 NaN           420.00  \n",
      "Coin                            NaN              NaN  \n",
      "El Corte Inglés                 NaN              NaN  \n"
     ]
    }
   ],
   "source": [
    "import yfinance as yf\n",
    "import pandas as pd\n",
    "import numpy as np\n",
    "\n",
    "print(\"Descargar datos da Yahoo Finance...\")\n",
    "macys = yf.Ticker(\"M\")\n",
    "amazon = yf.Ticker(\"AMZN\")\n",
    "marks_spencer = yf.Ticker(\"MKS.L\")\n",
    "\n",
    "df_macys_raw = macys.financials\n",
    "df_amazon_raw = amazon.financials\n",
    "df_markspencer_raw = marks_spencer.financials\n",
    "\n",
    "df_macys_bal = macys.balance_sheet\n",
    "df_amazon_bal = amazon.balance_sheet\n",
    "df_markspencer_bal = marks_spencer.balance_sheet\n",
    "\n",
    "\n",
    "macys_inc = df_macys_raw[df_macys_raw.columns[0]]\n",
    "amazon_inc = df_amazon_raw[df_amazon_raw.columns[0]]\n",
    "markspencer_inc = df_markspencer_raw[df_markspencer_raw.columns[0]]\n",
    "\n",
    "macys_bal = df_macys_bal[df_macys_bal.columns[0]]\n",
    "amazon_bal = df_amazon_bal[df_amazon_bal.columns[0]]\n",
    "markspencer_bal = df_markspencer_bal[df_markspencer_bal.columns[0]]\n",
    "\n",
    "print(\"alineación independiente de las tablas se ha completado con éxito!\\n\")\n",
    "\n",
    "\n",
    "dataset_retail = {}\n",
    "\n",
    "\n",
    "rev_amazon = amazon_inc.get('Total Revenue', np.nan)\n",
    "cogs_amazon = amazon_inc.get('Cost Of Revenue', np.nan)\n",
    "inv_amazon = amazon_bal.get('Inventory', np.nan)\n",
    "\n",
    "dataset_retail['Amazon'] = {\n",
    "    'Total Revenue ($)': rev_amazon,\n",
    "    'Gross Margin (%)': (amazon_inc.get('Gross Profit', np.nan) / rev_amazon) * 100 if pd.notna(rev_amazon) else np.nan,\n",
    "    'Operating Margin (%)': (amazon_inc.get('Operating Income', np.nan) / rev_amazon) * 100 if pd.notna(rev_amazon) else np.nan,\n",
    "    'EBITDA Margin (%)': (amazon_inc.get('EBITDA', np.nan) / rev_amazon) * 100 if pd.notna(rev_amazon) else np.nan,\n",
    "    'Cost of Revenue (%)': (cogs_amazon / rev_amazon) * 100 if pd.notna(rev_amazon) else np.nan,\n",
    "    'SG&A Margin (%)': (amazon_inc.get('Selling General And Administration', np.nan) / rev_amazon) * 100 if pd.notna(rev_amazon) else np.nan,\n",
    "    'Inventory Turnover': cogs_amazon / inv_amazon if pd.notna(inv_amazon) and inv_amazon != 0 else np.nan,\n",
    "    'Sales per Sq Ft': np.nan \n",
    "}\n",
    "\n",
    "rev_macys = macys_inc.get('Total Revenue', np.nan)\n",
    "cogs_macys = macys_inc.get('Cost Of Revenue', np.nan)\n",
    "inv_macys = macys_bal.get('Inventory', np.nan)\n",
    "\n",
    "dataset_retail[\"Macy's\"] = {\n",
    "    'Total Revenue ($)': rev_macys,\n",
    "    'Gross Margin (%)': (macys_inc.get('Gross Profit', np.nan) / rev_macys) * 100 if pd.notna(rev_macys) else np.nan,\n",
    "    'Operating Margin (%)': (macys_inc.get('Operating Income', np.nan) / rev_macys) * 100 if pd.notna(rev_macys) else np.nan,\n",
    "    'EBITDA Margin (%)': (macys_inc.get('EBITDA', np.nan) / rev_macys) * 100 if pd.notna(rev_macys) else np.nan,\n",
    "    'Cost of Revenue (%)': (cogs_macys / rev_macys) * 100 if pd.notna(rev_macys) else np.nan,\n",
    "    'SG&A Margin (%)': (macys_inc.get('Selling General And Administration', np.nan) / rev_macys) * 100 if pd.notna(rev_macys) else np.nan,\n",
    "    'Inventory Turnover': cogs_macys / inv_macys if pd.notna(inv_macys) and inv_macys != 0 else np.nan,\n",
    "    'Sales per Sq Ft': 180.00 \n",
    "}\n",
    "\n",
    "rev_markspencer = markspencer_inc.get('Total Revenue', np.nan)\n",
    "cogs_markspencer = markspencer_inc.get('Cost Of Revenue', np.nan)\n",
    "inv_markspencer = markspencer_bal.get('Inventory', np.nan)\n",
    "\n",
    "dataset_retail['Marks & Spencer'] = {\n",
    "    'Total Revenue ($)': rev_markspencer,\n",
    "    'Gross Margin (%)': (markspencer_inc.get('Gross Profit', np.nan) / rev_markspencer) * 100 if pd.notna(rev_markspencer) else np.nan,\n",
    "    'Operating Margin (%)': (markspencer_inc.get('Operating Income', np.nan) / rev_markspencer) * 100 if pd.notna(rev_markspencer) else np.nan,\n",
    "    'EBITDA Margin (%)': (markspencer_inc.get('EBITDA', np.nan) / rev_markspencer) * 100 if pd.notna(rev_markspencer) else np.nan,\n",
    "    'Cost of Revenue (%)': (cogs_markspencer / rev_markspencer) * 100 if pd.notna(rev_markspencer) else np.nan,\n",
    "    'SG&A Margin (%)': (markspencer_inc.get('Selling General And Administration', np.nan) / rev_markspencer) * 100 if pd.notna(rev_markspencer) else np.nan,\n",
    "    'Inventory Turnover': cogs_markspencer / inv_markspencer if pd.notna(inv_markspencer) and inv_markspencer != 0 else np.nan,\n",
    "    'Sales per Sq Ft': 420.00 \n",
    "}\n",
    "\n",
    "rev_coin = 169950000.00\n",
    "dataset_retail['Coin'] = {\n",
    "    'Total Revenue ($)': rev_coin,\n",
    "    'Gross Margin (%)': 43.50,          \n",
    "    'Operating Margin (%)': np.nan,      \n",
    "    'EBITDA Margin (%)': (-52000000.00 / rev_coin) * 100,\n",
    "    'Cost of Revenue (%)': 56.50,       \n",
    "    'SG&A Margin (%)': np.nan,           \n",
    "    'Inventory Turnover': np.nan,        \n",
    "    'Sales per Sq Ft': np.nan            \n",
    "}\n",
    "\n",
    "rev_eci = 15800000000.00\n",
    "dataset_retail['El Corte Inglés'] = {\n",
    "    'Total Revenue ($)': rev_eci,\n",
    "    'Gross Margin (%)': np.nan,          \n",
    "    'Operating Margin (%)': np.nan,      \n",
    "    'EBITDA Margin (%)': (1200000000.00 / rev_eci) * 100,\n",
    "    'Cost of Revenue (%)': np.nan,       \n",
    "    'SG&A Margin (%)': np.nan,          \n",
    "    'Inventory Turnover': np.nan,        \n",
    "    'Sales per Sq Ft': np.nan            \n",
    "}\n",
    "\n",
    "\n",
    "df_final = pd.DataFrame(dataset_retail).T\n",
    "columnas = [\n",
    "    'Total Revenue ($)', 'Gross Margin (%)', 'Cost of Revenue (%)', \n",
    "    'SG&A Margin (%)', 'Operating Margin (%)', 'EBITDA Margin (%)', \n",
    "    'Inventory Turnover', 'Sales per Sq Ft'\n",
    "]\n",
    "df_final = df_final[columnas]\n",
    "\n",
    "pd.set_option('display.float_format', lambda x: '%.2f' % x)\n",
    "\n",
    "print(\"--- DATASET COMPLETO PER IL TFM ---\")\n",
    "print(df_final)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "75fc46d9-8b7b-4aaa-87fe-120e36d3693d",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python [conda env:base] *",
   "language": "python",
   "name": "conda-base-py"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.13.9"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
