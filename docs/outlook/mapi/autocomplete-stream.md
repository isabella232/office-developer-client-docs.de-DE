---
title: Stream für automatisches Vervollständigen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: caa93fcc1675531f2d128170c81904e0e286e0f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591079"
---
# <a name="autocomplete-stream"></a>Stream für automatisches Vervollständigen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sie müssen nicht nur wissen, wie Microsoft Outlook mit dem Stream für automatisches Vervollständigen interagiert, sondern auch das Binärformat von AutoVervollständigen verstehen.
  
Der Stream für automatisches Vervollständigen besteht aus mehreren Zeilen mit Empfänger-Eigenschaften, die als binärer Stream zusammen mit einigen Verwaltungsmetadaten gespeichert und nur von Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 und Microsoft Outlook 2003 verwendet werden. Die Metadaten sind relevant für Outlook-Interaktionen mit dem Stream für automatisches Vervollständigen, sodass Dritte die Inhalte jedes Metadatenblocks beibehalten müssen, wenn sie einen geänderten Stream für automatisches Vervollständigen speichern. Dritte sollten also nur den Zeilensatz des Binärformats ändern und die Inhalte der Metadatenblöcke des Streams für automatisches Vervollständigen beibehalten.
  
## <a name="stream-visualization"></a>Stream-Visualisierung

Das allgemeine Layout des Streams für automatisches Vervollständigen lautet wie folgt:
  
Metadaten (4 Bytes)
  
Hauptversionsnummer (4 Bytes)
  
Nebenversionsnummer (4 Bytes)
  
Anzahl der Zeilen n (4 Bytes)
  
Anzahl der Eigenschaften p in der ersten Zeile (4 Bytes)
  
Tag der Eigenschaft 1 (4 Bytes)
  
Reservierte Daten der Eigenschaft 1 (4 Bytes)
  
Wertvereinigung der Eigenschaft 1 (8 Bytes)
  
Wertdaten der Eigenschaft 1 (0 oder variable Bytes)
  
… (Eigenschaft 2 bis Eigenschaft P-1)
  
Tag der Eigenschaft p (4 Bytes)
  
Reservierte Daten der Eigenschaft p (4 Bytes)
  
Wertvereinigung der Eigenschaft p (8 Bytes)
  
Wertdaten der Eigenschaft p (0 oder variable Bytes)
  
Anzahl der Eigenschaften q in der zweiten Zeile (4 Bytes)
  
… (Eigenschaften der zweiten Zeile)
  
… (Zeile 3 bis Zeile n-1)
  
Anzahl der Eigenschaften r in Zeile n (4 Bytes)
  
… (Eigenschaften der Zeile n)
  
Zusätzliche Informationen Byteanzahl EI (4 Bytes)
  
Zusätzliche Informationen (EI-Bytes)
  
Metadaten (8 Bytes)
  
Ein Beispiel für eine binäre Struktur finden Sie im Binärbeispiel in den [Outlook 2003/2007 NK2-Dateiformat- und Entwicklerrichtlinien.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
  
## <a name="high-level-layout"></a>Allgemeines Layout

Das allgemeine Layout des Streams für automatisches Vervollständigen lautet wie folgt:
  
|**Wertdaten**|**Anzahl der Bytes**|
|:-----|:-----|
|Metadaten  <br/> |4  <br/> |
|Nummer der Hauptversion  <br/> |4  <br/> |
|Nummer der Nebenversion  <br/> |4  <br/> |
|Zeilensatz  <br/> |Variable  <br/> |
|Zusätzliche Informationen Byteanzahl EI  <br/> |4  <br/> |
|Weitere Informationen  <br/> |EI  <br/> |
|Metadaten  <br/> |8  <br/> |
   
Wenn die Hauptversion nicht 12, sollte dieser Datenstrom nicht gelesen oder geschrieben werden. Die aktuelle Nebenversion des Streams für automatisches Vervollständigen ist 0, d. h. die Bytes für die zusätzlichen Informationen sind auf "0" festgelegt. Wenn die Nebenversion nicht 0 ist, befinden sich Informationen in den zusätzlichen Informationen, die beim Lesen des Streams gelesen und beim Schreiben des Streams beibehalten werden müssen. Die Nebenversion muss auch beim Schreiben des Streams beibehalten werden. Wenn beide nicht beibehalten werden, verlieren Instanzen von Outlook, die die zusätzlichen Informationen schreiben, Daten. 
  
> [!NOTE]
> Anwendungen dürfen keine benutzerdefinierten Daten zum Feld Zusätzliche Informationen hinzufügen und nicht die Nebenversion ändern, da diese Funktion Outlook-Erweiterungen des Formats und keine beliebigen Erweiterungen von Drittanbietern unterstützt. 
  
## <a name="row-set-layout"></a>Zeilensatz-Layout

Das Zeilensatz-Layout lautet wie folgt: 
  
|**Wertdaten**|**Anzahl der Bytes**|
|:-----|:-----|
|Anzahl der Zeilen  <br/> |4  <br/> |
|Zeilen  <br/> |Variable  <br/> |
   
Die Anzahl der Zeilen gibt an, wie viele Zeilen im nächsten Teil der binären Datenstromsequenz enthalten sind.
  
## <a name="row-layout"></a>Zeilen-Layout

Jede Zeile besitzt das folgende Format:
  
|**Wertdaten**|**Anzahl der Bytes**|
|:-----|:-----|
|Anzahl der Eigenschaften  <br/> |4  <br/> |
|Eigenschaften  <br/> |Variable  <br/> |
   
Die Anzahl der Eigenschaften gibt an, wie viele Eigenschaften im nächsten Teil der binären Datenstromsequenz enthalten sind.
  
## <a name="property-layout"></a>Eigenschaften-Layout

Jede Eigenschaft besitzt das folgende Format:
  
|**Wertdaten**|**Anzahl der Bytes**|
|:-----|:-----|
|Tag der Eigenschaft  <br/> |4  <br/> |
|Reservierte Daten  <br/> |4  <br/> |
|Eigenschaftswertvereinigung  <br/> ||
|Wertdaten  <br/> |0 oder Variable (abhängig vom Tag der Eigenschaft)  <br/> |
   
## <a name="interpreting-the-property-value"></a>Interpretation des Eigenschaftswerts

Die Eigenschaftswertvereinigung und die Wertdaten werden basierend auf dem Tag der Eigenschaft in den ersten 4 Bytes des Eigenschaftsblocks interpretiert. Das Tag der Eigenschaft liegt im selben Format vor wie das Tag der MAPI-Eigenschaft. Die Bits 0 bis 15 des Tags der Eigenschaft geben den Typ der Eigenschaft an. Die Bits 16 bis 31 sind Bezeichner der Eigenschaft. Der Eigenschaftentyp bestimmt, wie der Rest der Eigenschaft gelesen werden soll.
  
## <a name="static-value"></a>Statischer Wert

Einige Eigenschaften besitzen keine Wertdaten und verfügen nur in der Vereinigung über Daten. Die folgenden Eigenschaftstypen (die aus dem Eigenschafts-Tag stammen) sollten die 8 Byte Daten der Eigenschaftsvereinigung wie folgt interpretieren:
  
|**Eigenschaftstyp**|**Interpretation der Eigenschaftsvereinigung**|
|:-----|:-----|
|PT_I2  <br/> |short int  <br/> |
|PT_LONG  <br/> |long  <br/> |
|PT_R4  <br/> |float  <br/> |
|PT_DOUBLE  <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |short int  <br/> |
|PT_SYSTIME  <br/> |FILETIME  <br/> |
|PT_I8  <br/> |LARGE_INTEGER  <br/> |
   
## <a name="dynamic-values"></a>Dynamische Werte

Andere Eigenschaften weisen nach den 16 Bytes Daten in einem Wertdatenblock auf, die das Tag der Eigenschaft, die Reservierten Daten und die Eigenschaftswertvereinigung enthalten. Im Gegensatz zu statischen Werten sind die Daten, die in der 8-Byte-Eigenschaftswertvereinigung gespeichert sind, irrelevant für das Lesen. Stellen Sie beim Schreiben sicher, dass die 8 Bytes mit Werten gefüllt werden. Der Inhalt der 8 Bytes ist jedoch nicht wichtig. Bei dynamischen Werten bestimmt der Tagtyp der Eigenschaft die Interpretation der Wertdaten.
  
PT_STRING8 
  
|**Wertdaten**|**Anzahl der Bytes**|
|:-----|:-----|
|Anzahl der Bytes n  <br/> |4  <br/> |
|Bytes werden als ANSI-Zeichenfolge interpretiert (beinhaltet NULL-Abschlusszeichen)  <br/> |n  <br/> |
   
PT_CLSID
  
|**Wertdaten**|**Anzahl der Bytes**|
|:-----|:-----|
|Bytes, die als GUID interpretiert werden  <br/> |16  <br/> |
|||
   
PT_BINARY 
  
|**Wertdaten**|**Anzahl der Bytes**|
|:-----|:-----|
|Anzahl der Bytes n  <br/> |4  <br/> |
|Bytes, die als Byte-Array interpretiert werden  <br/> |n  <br/> |
   
PT_ERROR
  
|**Wertdaten**|**Anzahl der Bytes**|
|:-----|:-----|
|Anzahl der Bytes n  <br/> |4  <br/> |
|Bytes, die als Byte-Array interpretiert werden  <br/> |n  <br/> |
   
PT_MV_BINARY
  
|**Wertdaten**|**Anzahl der Bytes**|
|:-----|:-----|
|Anzahl der binären Arrays X  <br/> |4  <br/> |
|Eine Ausführung von Bytes, die X binäre Arrays enthält. Jedes Array sollten exakt wie die PT_BINARY-Byte-Ausführung interpretiert werden.  <br/> |Variable  <br/> |
   
PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)
  
|**Wertdaten**|**Anzahl der Bytes**|
|:-----|:-----|
|Anzahl der ANSI-Zeichenfolgen X  <br/> |4  <br/> |
|Eine Ausführung von Bytes, die X ANSI-Zeichenfolgen enthält. Jede Zeichenfolge sollte exakt wie die PT_STRING8-Byte-Ausführung interpretiert werden.  <br/> |Variable  <br/> |
   
PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)
  
|**Wertdaten**|**Anzahl der Bytes**|
|:-----|:-----|
|Anzahl der Unicode-Zeichenfolgen X  <br/> |4  <br/> |
|Eine Ausführung von Bytes, die X UNICODE-Zeichenfolgen enthält. Jede Zeichenfolge sollte exakt wie die PT_UNICODE-Byte-Ausführung interpretiert werden.  <br/> |Variable  <br/> |
   
## <a name="significant-properties"></a>Wesentliche Eigenschaften

Wie zuvor in diesem Artikel erwähnt, besitzen die binären Blöcke, die Eigenschaften darstellen, Eigenschafts-Tags, die Eigenschaften von Adressbuchempfängern entsprechen. Eine Beschreibung der Eigenschaften, die hier nicht aufgeführt sind, finden Sie unter http://msdn.microsoft.com/en-us/library/cc433490(EXCHG.80).aspx.
  
|**Eigenschaftsname**|**Eigenschafts-Tag**|**Beschreibung (weitere Informationen finden Sie unter MSDN)**|
|:-----|:-----|:-----|
|PR_NICK_NAME_W (nicht auf Empfänger übertragen, spezifisch für den Stream für automatisches Vervollständigen)  <br/> |0x6001001f  <br/> |Diese Eigenschaft muss in jeder Empfängerzeile zuerst stehen. Die Funktion dient als Schlüssel-ID für die Empfängerzeile.  <br/> |
|PR_ENTRYID  <br/> |0x0FFF0102  <br/> |Eintrag-ID des Adressbuchs für den Empfänger  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Anzeigename des Empfängers  <br/> |
|PR_EMAIL_ADDRESS_W  <br/> |0x3003001F  <br/> |E-Mail-Adresse des Empfängers (z. B. johndoe@contoso.com oder /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)  <br/> |
|PR_ADDRTYPE_W  <br/> |0x3002001F  <br/> |Adresstyp des Empfängers (z. B. SMTP oder EX).  <br/> |
|PR_SEARCH_KEY  <br/> |0x300B0102  <br/> |MAPI-Suchschlüssel des Empfängers  <br/> |
|PR_SMTP_ADDRESS_W  <br/> |0x39FE001f  <br/> |SMTP-Adresse des Empfängers  <br/> |
|PR_DROPDOWN_DISPLAY_NAME_W (nicht auf Empfänger übertragen, spezifisch für den Stream für automatisches Vervollständigen)  <br/> |0X6003001f  <br/> |Zeichenfolge, die in der AutoVervollständigen-Liste angezeigt wird  <br/> |
|PR_NICK_NAME_WEIGHT (nicht auf Empfänger übertragen, spezifisch für den Stream für automatisches Vervollständigen)  <br/> |0x60040003  <br/> |Gewichtung dieses AutoVervollständigen-Eintrags Mit der Gewichtung wird bestimmt, in welcher Reihenfolge AutoVervollständigen-Einträge beim Abgleich der AutoVervollständigen-Liste ausgeführt werden. Einträge mit höherer Gewichtung werden vor Einträgen mit geringerer Gewichtung angezeigt. Die komplette AutoVervollständigen-Liste wird nach dieser Eigenschaft sortiert. Die Gewichtung wird in regelmäßigen Abständen über einen Zeitraum verringert und wird vergrößert, wenn der Benutzer eine E-Mail-Nachricht an diesen Empfänger sendet. Weitere Informationen zu dieser Eigenschaft finden Sie weiter unten in diesem Thema.  <br/> |
   
PR_NICK_NAME_WEIGHT
  
Der Zeilensatz dieses Streams für automatisches Vervollständigen ist in absteigender Reihenfolge nach der Eigenschaft PR_NICK_NAME_WEIGHT sortiert, und der Stream für automatisches Vervollständigen sollte dieses Sortierverhalten immer beibehalten. Aus diesem Grund sollte bei Änderungen an der Gewichtung einer Zeile sichergestellt werden, dass die Position der Zeile die Sortierreihenfolge des kompletten Zeilensatzes beibehält. Zusätze zum Zeilensatz sollten an der richtigen Stelle eingefügt werden, um die Sortierreihenfolge beizubehalten.
  
Der Mindestwert für diese Gewichtung ist 0x1, und der Maximalwert beträgt LONG_MAX. Alle anderen Werte für die Gewichtung werden als ungültig betrachtet.
  
Wenn Outlook 2007 eine E-Mail an einen Empfänger versendet oder einen Empfänger auflöst, wird die Gewichtung dieses Empfängers um 0x2000 erhöht.
  

