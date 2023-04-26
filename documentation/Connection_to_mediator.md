### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Startseite](/documentation/documentation.md)
<br><br>

# Anbindung an den Vermittlungsdienst
Es gibt zwei Möglichkeiten Bekanntmachungen an den Vermittlungsdienst zu übermitteln, per [REST API](#anbindung-per-rest-api) oder mit Hilfe des [eDelivery Network PEPPOL](#anbindung-per-peppol-in-der-umsetzung) (in der Umsetzung).
<br><br>

## Anbindung per REST API
Der Vermittlungsdienst stellt eine REST API zur Verfügung, die von jeder Vergabeplattform genutzt werden kann, um Bekanntmachungen an den Vermittlungsdienst zu übermitteln.<br><br>
Zur Authentifizierung wird ein entsprechender Token benötigt, welcher mit Hilfe Ihrer Zugangsdaten über unsere API generiert werden kann. Folgen Sie hierzu den unter [Beantragen eines Zugangs durch einen FVH](#beantragen-eines-zugangs-durch-einen-fvh) beschriebenen Schritten, um einen Nutzeraccount für ihre E-Mail-Adresse anlegen zu lassen und ein Passwort zu setzen. Die Dokumentation zur Mediator API zum Abrufen des Tokens finden sie unter https://bkms-mediator-app-preview.efa-fhb.apps-int.nortal.com.
<br><br>

## Anbindung per PEPPOL (in der Umsetzung)
Es ist zukünftig möglich Bekanntmachungen auch über das eDelivery Network PEPPOL an den Vermittlungsdienst zu übermitteln. Details und weitere Informationen folgen. 
<br><br>

## Beantragen eines Zugangs durch einen FVH
Ein Vertreter des FVH beantragt die Einrichtung eines neuen Benutzer per E-Mail an oeffentliche-vergabe@nortal.com bei der Nortal AG. Es muss pro Vergabeplattform ein Benutzer angelegt werden.<br>
In der E-Mail müssen folgende Angaben enthalten sein:

- Benutzer E-Mail-Adresse welche als Benutzername verwendet werden soll
- URL der Vergabeplattform
- Vor- und Nachname sowie die E-Mail-Adresse des Vertreters des FVH
- Name des FVH

Nach der Erstellung des Benutzers wird zur Überprüfung an die angegebene Benutzer E-Mail-Adresse eine Bestätigungs-E-Mail versendet. Außerdem enthält die E-Mail einen Link zur Erstellung des Passworts.
<br><br>
Der Link ist 24 Stunden lang gültig.<br>
Das Passwort muss aus mindestens 8 Zeichen bestehen, 1 Großbuchstaben und 1 Zahl enthalten.
<br><br>
Mit den erstellten Zugangsdaten können Sie mit Hilfe der Mediator API (https://bkms-mediator-app-preview.efa-fhb.apps-int.nortal.com.) einen entsprechenden Token generieren.
<br><br>

## Wie setzt man ein Benutzer Passwort zurück?
1. Anmeldeseite aufrufen<br>
Testumgebung. https://keycloak-preview.efa-fhb.apps-int.nortal.com/realms/ozg-vermittlungsdienst/account/#/ → Auf 'Anmelden' klicken<br>
![Anmeldeseite aufrufen](images/kc_anmeldeseite.png)
<br><br>

2. Auf 'Passwort vergessen?' klicken<br>
![Auf Passwort vergessen](images/kc_login.png)
<br><br>

3. E-Mail-Adresse eintragen und auf 'Absenden' klicken<br>
![E-Mail eintragen](images/kc_passwort_vergessen.png)
<br><br>

4. Die Meldung 'Sie sollten in Kürze eine E-Mail mit weiteren Instruktionen erhalten' wir angezeigt.<br>
![Meldung](images/kc_nachricht_best%C3%A4tigungsemail.png)
<br><br>

5. Überprüfen der E-Mails: Ein Link zum Zurücksetzen der Anmeldeinformationen ist in der E-Mail erhalten.<br>
![Bestätigungs-E-Mail](images/e-mail_passwort_zuruecksetzen.png)
<br><br>

6. Auf 'Link zum Zurücksetzen von Anmeldeinformationen' klicken.
<br><br>

7. Der Benutzer wird auf die Seite 'Passwort aktualisieren' umgeleitet.<br>
![PAsswort aktualisieren](images/kc_passwort_aktualisieren.png)
<br><br>

8. Neues Passwort eintragen und bestätigen und auf 'Absenden' klicken.<br>
Das Passwort muss aus mindestens 8 Zeichen bestehen, 1 Großbuchstaben und 1 Zahl enthalten.
<br><br>

9. Das Passwort muss in der FVH-Software hinterlegt werden um sicher zu gehen, dass die Verbindung mit dem Vermittlungsdienst funktioniert.