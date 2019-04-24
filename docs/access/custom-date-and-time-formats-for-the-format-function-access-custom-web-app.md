---
title: Benutzerdefinierte Datums- und Uhrzeitformate für die Format-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.assetid: f7d15fe6-bdad-4f1f-aa18-12a21fc111c4
description: Informationen zum Steuern der Anzeige eines Datums oder einer Uhrzeit durch eine benutzerdefinierte Formatierung.
localization_priority: Priority
ms.openlocfilehash: 76ba7361be4f7902a3ee4a1a8d6e51211ad114bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282208"
---
# <a name="custom-date-and-time-formats-for-the-format-function-access-custom-web-app"></a>Benutzerdefinierte Datums- und Uhrzeitformate für die Format-Funktion (benutzerdefinierte Access-Web-App)

Informationen zum Steuern der Anzeige eines Datums oder einer Uhrzeit durch eine benutzerdefinierte Formatierung.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-DE/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="format-specifications"></a>Formatspezifikationen

In der folgenden Tabelle werden Zeichen aufgeführt, die Sie in Verbindung mit der [Format-Funktion (Access benutzerdefinierte Web app)](format-function-access-custom-web-app.md)-Funktion zum Erstellen von benutzerdefinierten Datums- und Uhrzeitformaten verwenden können. 
  
|**Formatangabe**|**Beschreibung**|
|:-----|:-----|
|(:)  <br/> |Zeittrennzeichen. In manchen Gebietsschemas werden andere Zeichen als Zeittrennzeichen verwendet. Das Zeittrennzeichen trennt Stunden, Minuten und Sekunden bei der Formatierung von Zeitwerten. Das tatsächliche in der formatierten Ausgabe als Zeittrennzeichen verwendete Zeichen wird durch den aktuellen Kulturwert Ihrer Anwendung bestimmt.  <br/> |
|(/)  <br/> |Datumstrennzeichen. In manchen Gebietsschemas werden andere Zeichen als Datumstrennzeichen verwendet. Das Datumstrennzeichen trennt Tag, Monat und Jahr bei der Formatierung von Datumswerten. Das tatsächliche in der formatierten Ausgabe als Datumstrennzeichen verwendete Zeichen wird durch den aktuellen Kulturwert Ihrer Anwendung bestimmt.  <br/> |
|(%)  <br/> |Legt fest, dass das folgende Zeichen ohne Rücksicht auf nachfolgende Buchstaben im Einzelbuchstabenformat ausgelesen werden soll. Damit kann außerdem angegeben werden, dass ein Einzelbuchstabenformat als benutzerdefiniertes Format ausgelesen werden soll. Die Informationen unten enthalten weitere Informationen zu diesem Thema.  <br/> |
|d  <br/> |Zeigt den Tag als Zahl ohne führende Null an (Beispiel: 1). Verwenden Sie %d, wenn dies das einzige Zeichen im benutzerdefinierten Zahlenformat ist.  <br/> |
|dd  <br/> |Zeigt den Tag als Zahl mit einer führenden Null an (Beispiel: 01).  <br/> |
|ddd  <br/> |Zeigt den Tag als Abkürzung an (z. B. Sun).  <br/> |
|dddd  <br/> |Zeigt den Tag in ausgeschriebener Schreibweise an (z. B. Sonntag).  <br/> |
|M  <br/> |Zeigt den Monat als Zahl ohne führende Null an (Januar wird z. B. durch 1 dargestellt). Verwenden Sie "%M", wenn dies das einzige Zeichen im benutzerdefinierten Zahlenformat ist.  <br/> |
|MM  <br/> |Zeigt den Monat als Zahl mit einer führenden Null an (z. B. 12.01.01).  <br/> |
|MMM  <br/> |Zeigt den Monat als Abkürzung an (z. B. Jan).  <br/> |
|MMMM  <br/> |Zeigt den Monat als vollständigen Monatsnamen an (z. B. Januar).  <br/> |
|gg  <br/> |Zeigt die Zeichenfolge Zeitraum an (z. B. n. Chr.).  <br/> |
|h  <br/> |Zeigt die Stunde als Zahl ohne führende Nullen im 12-Stunden-Format an (z. B. 1:15:15 PM). Verwenden Sie "%h", wenn dies das einzige Zeichen im benutzerdefinierten Zahlenformat ist.  <br/> |
|hh  <br/> |Zeigt die Stunde als Zahl mit führenden Nullen im 12-Stunden-Format an (z. B. 01:15:15 PM).  <br/> |
|H  <br/> |Zeigt die Stunde als Zahl ohne führende Nullen im 24-Stunden-Format an (z. B. 13:15:15). Verwenden Sie "%H", wenn dies das einzige Zeichen im benutzerdefinierten Zahlenformat ist.  <br/> |
|HH  <br/> |Zeigt die Stunde als Zahl mit führenden Nullen im 24-Stunden-Format an (z. B. 01:15:15).  <br/> |
|m  <br/> |Zeigt die Minute als Zahl ohne vorangestellte Null an (z. B. 12:1:15). Verwenden Sie "%m", wenn dies das einzige Zeichen im benutzerdefinierten Zahlenformat ist.  <br/> |
|mm  <br/> |Zeigt die Minute als Zahl mit führenden Nullen an (z. B. 12:01:15).  <br/> |
|s  <br/> |Zeigt die Sekunde als Zahl ohne vorangestellte Null an (z. B. 12:15:5). Verwenden Sie "%s", wenn dies das einzige Zeichen im benutzerdefinierten Zahlenformat ist.  <br/> |
|ss  <br/> |Zeigt die Sekunde als Zahl mit führenden Nullen an (z. B. 12:15:05).  <br/> |
|f  <br/> |Zeigt Sekundenbruchteile an. Beispielsweise zeigt ff Hundertstel Sekunden und ffff Zehntausendstel Sekunden an. Ihr benutzerdefiniertes Format darf aus bis zu sieben f bestehen. Verwenden Sie %f, wenn dies das einzige Zeichen im benutzerdefinierten Zahlenformat ist.  <br/> |
|t  <br/> |Verwendet das 12-Stunden-Format und zeigt ein großes A für jede Stunde vor Mittag; Zeigt ein großes P für jede Stunde zwischen Mittag und 23:59 Uhr. Verwenden Sie "%t", wenn dies das einzige Zeichen im benutzerdefinierten Zahlenformat ist.  <br/> |
|tt  <br/> |Für Gebietsschemas, die das 12-Stunden-Format verwenden, wird für jede Stunde vor Mittag "AM" in Großbuchstaben angezeigt; Zeigt die Großbuchstaben "PM" für jede Stunde zwischen Mittag und 23:59 Uhr an.  <br/> Für Gebietsschemas, die das 24-Stunden-Format verwenden, wird nichts angezeigt.  <br/> |
|y  <br/> |Zeigt die Jahreszahl (0-9) ohne führende Nullen an. Verwenden Sie "%y", wenn dies das einzige Zeichen im benutzerdefinierten Zahlenformat ist.  <br/> |
|yy  <br/> |Zeigt das Jahr im zweistelligen Format mit einer führenden Null an, falls zutreffend.  <br/> |
|yyy  <br/> |Zeigt das Jahr als vierstellige Zahl an.  <br/> |
|yyyy  <br/> |Zeigt das Jahr als vierstellige Zahl an.  <br/> |
||Zeigt den Zeitzonenunterschied ohne führende Null an (Beispiel: -8). Verwenden Sie "%z", wenn dies das einzige Zeichen im benutzerdefinierten Zahlenformat ist.  <br/> |
|z  <br/> |Zeigt den Zeitzonenunterschied mit einer führenden Null an (z. B. -08).  <br/> |
|zz  <br/> |Zeigt den Zeitzonenunterschied mit einer führenden Null an (z. B.-08)  <br/> |
|zzz  <br/> |Zeigt den vollständigen Zeitzonenunterschied an (z. B. -08:00)  <br/> |
   
## <a name="remarks"></a>Hinweise

Bei Formatierungszeichenfolgen werden Groß- und Kleinschreibung unterschieden. Mit Groß- und Kleinbuchstaben können unterschiedliche Formatierungen abgerufen werden. Beispielsweisewird bei der Formatierung eines Datumswerts mit der Zeichenfolge "D" ein Datum in Langform ausgegeben (entsprechend dem aktuellen Gebietsschema), während mit "d" die Kurzform ausgegeben wird. Darüber hinaus können unerwartete Ergebnisse oder Fehler auftreten, wenn die gewünschte Formatierung nicht mit der Schreibweise der jeweiligen definierten Formatzeichenfolge übereinstimmt.
  
## <a name="see-also"></a>Siehe auch

- [Format-Funktion (benutzerdefinierte Access-Web-App)](format-function-access-custom-web-app.md) 
- [Benutzerdefinierte numerische Formate für die Format-Funktion (benutzerdefinierte Access-Web-App)](custom-numeric-formats-for-the-format-function-access-custom-web-app.md)
  

