1. Priprema i inženjerstvo podataka (Data Preprocessing)
Čišćenje: Uklonjeni su irelevantni stupci poput ID-a i poštanskog broja kako bi se izbjegao šum u podacima.
Nove značajke: Iz datuma prodaje i godine gradnje izvedena je starost nekretnine (house_age), a renovacija je pretvorena u binarnu varijablu.
Skaliranje: Podaci su standardizirani (StandardScaler), što je ključno za stabilnost neuronskih mreža.

2. Analiza podataka (EDA)
Korelacija: Matrica korelacije potvrdila je da su kvadratura stambenog prostora i ocjena gradnje (grade) najjače povezani s cijenom.
Geografija: Vizualizacija latitude i longitude otkrila je jasne prostorne klastere visoke vrijednosti nekretnina.

4. Modeliranje i rezultati
Uspoređena su četiri modela: Linearna regresija, Random Forest, XGBoost i Umjetna neuronska mreža (ANN).
Pobjednik: Ansambl modeli (XGBoost i Random Forest) postigli su najveću preciznost s $R^2 \approx 0.88$, 
što znači da objašnjavaju 88% varijacije u cijeni.ANN je pokazao dobre rezultate uz korištenje Dropout slojeva za sprječavanje preučenja.

4. Interpretacija i uvid (Explainable AI)
SHAP analiza: Korištena je moderna metoda Shapley vrijednosti kako bi se točno vidjelo koliko svaki parametar (npr. pogled, lokacija) dodaje ili oduzima od konačne cijene.
Važnost značajki: Utvrđeno je da su kvaliteta gradnje (grade) i lokacija (lat) često presudniji faktori od samog broja soba.
Analiza grešaka: Detaljno su ispitani rubni slučajevi (najveći promašaji) kako bi se utvrdila ograničenja modela kod ekstremno luksuznih nekretnina

Zaključak
Projekt dokazuje da moderni algoritmi strojne inteligencije mogu vrlo precizno procijeniti tržišnu vrijednost nekretnina,
pri čemu su geografski podaci i kvaliteta izvedbe ključni faktori preciznosti.

Dataset -> https://www.kaggle.com/datasets/sukhmandeepsinghbrar/housing-price-dataset?resource=download
