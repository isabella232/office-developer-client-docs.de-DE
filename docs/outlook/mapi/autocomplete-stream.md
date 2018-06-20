---
title: AutoVervollständigen-Stream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7fc1fae4ed648d59c273b20ced247f6d20e01a6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791354"
---
# <a name="autocomplete-stream"></a>AutoVervollständigen-Stream

  
  
**Betrifft**: Outlook 
  
Zusätzlich zu wissen, wie Microsoft Outlook mit den AutoVervollständigen-Stream interagiert, müssen Sie auch das Binärformat des Datenstroms AutoVervollständigen verstehen.
  
Die AutoVervollständigen-Datenstrom ist ein Satz von Zeilen Empfänger-Eigenschaft, die als einen binären Datenstrom zusammen mit einigen Metadaten, die Buchhaltung gespeichert sind, die nur von Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 und Microsoft Outlook 2003 verwendet wird. Die Metadaten ist Outlook Interaktionen mit dem AutoVervollständigen-Stream für die Überprüfung relevante, sodass dritte beibehalten müssen, was in jedem Metadaten-Block ist, wenn sie einen geänderte AutoVervollständigen-Stream speichern. Anders ausgedrückt, sollten dritte nur den Zeile Set Teil der Binärformat ändern und beibehalten, was bereits in der die Metadaten-Blöcke des Datenstroms AutoVervollständigen ist.
  
## <a name="stream-visualization"></a>Stream Visualisierung

Das allgemeine Layout des Datenstroms AutoVervollständigen lautet wie folgt:
  
Metadaten (4 Bytes)
  
Nummer der Hauptversion (4 Bytes)
  
Minor Versionsnummer (4 Bytes)
  
Anzahl der Zeilen n (4 Bytes)
  
Anzahl der Eigenschaften p in Zeile 1 (4 Bytes)
  
Eigenschafts-Tag 1-Eigenschaft (4 Bytes)
  
1-Eigenschaft des Daten (4 Bytes) reserviert.
  
Eigenschaft 1 Wert Union (8 Byte)
  
Wertdaten 1 Eigenschaft (0 oder Variable Bytes)
  
… (über-Eigenschaft P-1-Eigenschaft 2)
  
Eigenschaft p des Eigenschafts-Tag (4 Bytes)
  
Eigenschaft p der Daten (4 Bytes) reserviert.
  
Eigenschaft p Wert Union (8 Byte)
  
Eigenschaft p des Wertdaten (0 oder Variable Bytes)
  
Anzahl der Eigenschaften Q in Zeile 2 (4 Bytes)
  
… (die zweite Zeileneigenschaften)
  
… (Zeile 3 über Zeile n-1)
  
Anzahl der Eigenschaften R in Zeile n (4 Bytes)
  
… (Zeile n's Eigenschaften)
  
Zusätzliche Informationen Byteanzahl EI (4 Bytes)
  
Zusätzliche Informationen (EI Bytes)
  
Metadaten (8 Byte)
  
Ein Beispiel für eine binäre Struktur, finden Sie unter Binary für das Beispiel in der [Outlook 2003/2007 NK2-Dateiformat und Richtlinien für Entwickler.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
  
## <a name="high-level-layout"></a>Allgemeine Layout

Generell wird das Layout des Datenstroms AutoVervollständigen wie folgt:
  
|**Wertdaten**|**Anzahl von Bytes**|
|:-----|:-----|
|Metadaten  <br/> |4  <br/> |
|Nummer der Hauptversion  <br/> |4  <br/> |
|Nummer der Nebenversion  <br/> |4  <br/> |
|Rowset-fest  <br/> |Variable  <br/> |
|Zusätzliche Informationen Byteanzahl EI  <br/> |4  <br/> |
|Zusätzliche Informationen  <br/> |EI  <br/> |
|Metadaten  <br/> |8  <br/> |
   
Wenn dieser Datenstrom lesen, wenn die Hauptversion 12 unterscheidet, sollte klicken Sie dann diesen Datenstrom nicht lesen oder schreiben. Die aktuelle Nebenversion des Datenstroms AutoVervollständigen ist 0, womit die zusätzlichen Informationen Byteanzahl auf 0 festgelegt wurde. Wenn die Nebenversion 0 unterscheidet, wird die Informationen in die zusätzlichen Informationen, die beim Lesen der Streams lesen und beim Schreiben des Streams beibehalten werden muss vorhanden sein. Die Nebenversion müssen auch beim Schreiben des Streams beibehalten werden soll. Wenn beide nicht beibehalten werden, verlieren Instanzen von Outlook, die die zusätzliche Informationen geschrieben haben Daten. 
  
> [!NOTE]
> Applikationen dürfen keine benutzerdefinierte Daten in das Feld zusätzliche Informationen hinzufügen oder ändern die Nebenversion, wie diese Funktionalität zur Unterstützung von Outlook-Erweiterungen für das Format und nicht beliebige Drittanbieter-Erweiterungen ist. 
  
## <a name="row-set-layout"></a>Rowset Layout

Das Layout Rowset lautet wie folgt: 
  
|**Wertdaten**|**Anzahl von Bytes**|
|:-----|:-----|
|Anzahl von Zeilen  <br/> |4  <br/> |
|Rows  <br/> |Variable  <br/> |
   
Die Anzahl der Zeilen identifiziert, wie viele Zeilen in der nächsten Teil der Sequenz binären Stream stammen.
  
## <a name="row-layout"></a>Zeilenlayout

Jede Zeile hat Folgendes Format:
  
|**Wertdaten**|**Anzahl von Bytes**|
|:-----|:-----|
|Anzahl der Eigenschaften  <br/> |4  <br/> |
|Eigenschaften  <br/> |Variable  <br/> |
   
Die Anzahl der Eigenschaften bestimmt, wie viele Eigenschaften in der nächsten Teil der Sequenz binären Stream stammen.
  
## <a name="property-layout"></a>Eigenschaft Layout

Jede Eigenschaft hat das folgende Format:
  
|**Wertdaten**|**Anzahl von Bytes**|
|:-----|:-----|
|Eigenschafts-Tag  <br/> |4  <br/> |
|Reservierte Daten  <br/> |4  <br/> |
|Eigenschaft Wert Union  <br/> ||
|Wertdaten  <br/> |0 oder Variable (je nach Eigenschaft-Tag)  <br/> |
   
## <a name="interpreting-the-property-value"></a>Interpretieren den Eigenschaftswert

Die Union-Eigenschaft Wert und die Daten des Werts sind interpretiert werden das Eigenschafts-Tag in den ersten 4 Byte des Blocks Eigenschaft basierend auf. Dieses Eigenschaftentag befindet sich in demselben Format wie ein MAPI-Eigenschaftentag. Bits 0 bis 15 des Eigenschaftstags sind den Typ der Eigenschaft. Bits 16 bis 31 sind die Eigenschaft Bezeichner. Der Eigenschaftstyp bestimmt, wie die-Eigenschaft die restlichen gelesen werden sollen.
  
## <a name="static-value"></a>Statische Wert

Einige Eigenschaften haben keine Wertdaten und haben nur Daten in der Union. Die folgenden Eigenschaftentypen (die aus dem Tag-Eigenschaft stammen) sollte die Union-Eigenschaft 8-Byte-Daten wie folgt interpretiert werden:
  
|**Eigenschaft Type**|**Eigenschaft Union Interpretation**|
|:-----|:-----|
|PT_I2  <br/> |kurze int  <br/> |
|PT_LONG  <br/> |long  <br/> |
|PT_R4  <br/> |Gleitkommazahl  <br/> |
|PT_DOUBLE  <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |kurze int  <br/> |
|PT_SYSTIME  <br/> |FILETIME  <br/> |
|PT_I8  <br/> |LARGE_INTEGER  <br/> |
   
## <a name="dynamic-values"></a>Dynamische Werte

Andere Eigenschaften aufweisen Daten in einem Wert Datenblock, nachdem die ersten 16 Bytes, die die Tag-Eigenschaft, die reservierte Daten und der Union-Eigenschaft Wert enthalten. Im Gegensatz zu statische Werte spielt die Daten, die in der 8-Byte-Eigenschaftswert Union gespeichert werden beim Lesen. Beim Schreiben, stellen Sie sicher, dass diese 8 Bytes mit etwas zu füllen. Der Inhalt von 8 Bytes ist jedoch nicht wichtig. Dynamische Werte bestimmt das Eigenschafts-Tag-Typ wie die Daten des Werts interpretiert werden.
  
PT_STRING8 
  
|**Wertdaten**|**Anzahl von Bytes**|
|:-----|:-----|
|Anzahl von Bytes n  <br/> |4  <br/> |
|Bytes als ANSI-Zeichenfolge interpretiert werden soll (einschließlich der NULL-Terminator)  <br/> |n  <br/> |
   
PT_CLSID
  
|**Wertdaten**|**Anzahl von Bytes**|
|:-----|:-----|
|Bytes als GUID interpretiert werden soll  <br/> |16  <br/> |
|||
   
PT_BINARY 
  
|**Wertdaten**|**Anzahl von Bytes**|
|:-----|:-----|
|Anzahl von Bytes n  <br/> |4  <br/> |
|Bytes als Bytearray interpretiert werden soll  <br/> |n  <br/> |
   
PT_ERROR
  
|**Wertdaten**|**Anzahl von Bytes**|
|:-----|:-----|
|Anzahl von Bytes n  <br/> |4  <br/> |
|Bytes als Bytearray interpretiert werden soll  <br/> |n  <br/> |
   
PT_MV_BINARY
  
|**Wertdaten**|**Anzahl von Bytes**|
|:-----|:-----|
|Anzahl der binären Arrays X  <br/> |4  <br/> |
|Ausführung von Bytes, die X enthält binäre Arrays. Jedes Array sollte genau wie das Ausführen PT_BINARY Byte interpretiert werden.  <br/> |Variable  <br/> |
   
PT_MV_STRING8 (Outlook 2007, Outlook 2010 und Outlook 2013)
  
|**Wertdaten**|**Anzahl von Bytes**|
|:-----|:-----|
|Anzahl von ANSI-Zeichenfolgen X  <br/> |4  <br/> |
|Ein Lauf von Bytes, die X-ANSI-Zeichenfolgen enthält. Jede Zeichenfolge sollte genau wie das Ausführen PT_STRING8 Byte interpretiert werden.  <br/> |Variable  <br/> |
   
PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)
  
|**Wertdaten**|**Anzahl von Bytes**|
|:-----|:-----|
|Anzahl der Unicode-Zeichenfolgen X  <br/> |4  <br/> |
|Ein Lauf von Bytes, die X UNICODE Zeichenfolgen enthält. Jede Zeichenfolge sollte genau wie das Ausführen PT_UNICODE Byte interpretiert werden.  <br/> |Variable  <br/> |
   
## <a name="significant-properties"></a>Wesentliche Eigenschaften

Wie zuvor in diesem Thema erwähnt, müssen die binären Blöcke, die Eigenschaften darstellen Eigenschaftentags, die die Eigenschaften Address Book Empfänger entsprechen. Für Eigenschaften, die hier nicht aufgeführt sind, können Sie Nachschlagen der Beschreibung unter http://msdn.microsoft.com/en-us/library/cc433490(EXCHG.80).aspx.
  
|**Eigenschaftenname**|**Eigenschafts-Tag**|**Beschreibung (Weitere Informationen finden Sie unter MSDN)**|
|:-----|:-----|:-----|
|PR_NICK_NAME_W (nicht auf in AutoVervollständigen-Stream nur bestimmte Empfänger gesendeten)  <br/> |0x6001001f  <br/> |Diese Eigenschaft muss in jeder Zeile Empfänger ersten sein. Es dient funktional als eine Schlüssel-ID für die Empfänger Zeile.  <br/> |
|PR_ENTRYID  <br/> |0x0FFF0102  <br/> |Der Address Book Eintrag Bezeichner für den Empfänger.  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Der Name des Empfängers anzeigen.  <br/> |
|PR_EMAIL_ADDRESS_W  <br/> |0x3003001F  <br/> |E-Mail-Adresse des Empfängers (z. B. johndoe@contoso.com oder/o = Contoso/OU = "Foo" / Cn = Recipients/Cn = Johndoe)  <br/> |
|PR_ADDRTYPE_W  <br/> |0x3002001F  <br/> |Der Empfänger Adresstyp (z. B. SMTP oder EX).  <br/> |
|PR_SEARCH_KEY  <br/> |0x300B0102  <br/> |Der Empfänger MAPI-Suchen-Taste.  <br/> |
|PR_SMTP_ADDRESS_W  <br/> |0x39FE001f  <br/> |SMTP-Adresse des Empfängers.  <br/> |
|PR_DROPDOWN_DISPLAY_NAME_W (nicht auf in AutoVervollständigen-Stream nur bestimmte Empfänger gesendeten)  <br/> |0X6003001f  <br/> |Die Zeichenfolge, die in der AutoVervollständigen-Liste angezeigt wird.  <br/> |
|PR_NICK_NAME_WEIGHT (nicht auf in AutoVervollständigen-Stream nur bestimmte Empfänger gesendeten)  <br/> |0x60040003  <br/> |Die Stärke des in AutoVervollständigen-Eintrag. Die Gewichtung wird verwendet, um zu bestimmen, in welcher Reihenfolge AutoVervollständigen Einträge auftreten, wenn die AutoVervollständigen-Liste entsprechen. Einträge mit höheren Gewichtung werden vor Einträgen mit geringeren Gewichtung angezeigt. Die vollständige AutoVervollständigen-Liste wird von dieser Eigenschaft sortiert. Die Gewichtung in regelmäßigen Abständen nimmt mit der Zeit und erhöht, wenn der Benutzer eine e-Mail an diesen Empfänger sendet. Siehe Beschreibung weiter unten in diesem Thema für Weitere Informationen zu dieser Eigenschaft.  <br/> |
   
PR_NICK_NAME_WEIGHT
  
Der Satz von Zeilen im Datenstrom AutoVervollständigen wird von der PR_NICK_NAME_WEIGHT-Eigenschaft in absteigender Reihenfolge sortiert und des AutoVervollständigen-Streams sollte immer dieses sortierte Merkmal beibehalten. Aus diesem Grund sollten Änderungen an einer Zeile Gewichtung auch Stellen Sie sicher, dass die Zeilenposition wird die Sortierreihenfolge der der vollständige Satz von Zeilen verwaltet. Hinzufügen der Zeile-Set sollte auf die richtige Position zur Aufrechterhaltung der Sortierreihenfolge eingefügt werden.
  
Der Mindestwert für dieses Gewicht ist 0 x 1 und der Höchstwert ist LONG_MAX. Alle anderen Werte für die Gewichtung gelten als ungültig.
  
Wenn Outlook 2007 sendet eine e-Mail an oder löst einen Empfänger wird es Stärke des Empfängers um 0 x 2000 erhöht.
  

