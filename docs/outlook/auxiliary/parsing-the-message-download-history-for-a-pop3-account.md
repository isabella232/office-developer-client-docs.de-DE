---
title: Analysieren des Nachrichtendownloadverlaufs für ein POP3-Konto
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: In diesem Thema wird die Struktur des POP3-BLOB beschrieben, das den Nachrichtendownloadverlauf eines POP3-Kontos darstellt, um die Nachrichten zu identifizieren, die für dieses Konto heruntergeladen oder gelöscht wurden.
ms.openlocfilehash: 44a799f6b6fbe2a2841522c18405149a470b0236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327763"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a>Analysieren des Nachrichtendownloadverlaufs für ein POP3-Konto

In diesem Thema wird die Struktur des POP3-BLOB beschrieben, das den Nachrichtendownloadverlauf eines POP3-Kontos darstellt, um die Nachrichten zu identifizieren, die für dieses Konto heruntergeladen oder gelöscht wurden.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a>

## <a name="why-parse-the-message-download-history"></a>Warum sollte der Nachrichtendownloadverlauf analysiert werden?

Der Post Office Protocol (POP)-Anbieter für Outlook ermöglicht Benutzern das Abrufen und Herunterladen neuer E-Mail-Nachrichten auf ihrem lokalen Gerät und anschließend das Verlassen oder Löschen dieser E-Mail-Nachrichten auf dem E-Mail-Server. Wenn der E-Mail-Client überprüft, ob neue Nachrichten heruntergeladen werden sollen, muss er nur die neuen Nachrichten für diesen Posteingang identifizieren und herunterladen können. Der E-Mail-Client verwendet dazu zunächst den Befehl UIDL (Unique ID Listing), um eine Karte jeder Nachricht zu erhalten, die jemals an diesen Posteingang an einen eindeutigen Bezeichner (Unique Identifier, UID) zugestellt wurde. Der Client ruft außerdem den Nachrichtendownloadverlauf für Nachrichten ab, die für den Posteingang auf diesem Client heruntergeladen oder gelöscht wurden. Mithilfe der UiD-Karte und des Downloadverlaufs der Nachricht kann der Client dann die Nachrichten identifizieren, die im Verlauf nicht vorhanden sind, als neu und sollten daher heruntergeladen werden.
  
So erhalten Sie den Nachrichtendownloadverlauf für einen Posteingang:
  
- Führen Sie die Schritte unter Suchen des Nachrichtendownloadverlaufs für ein [POP3-Konto](locating-the-message-download-history-for-a-pop3-account.md) aus, um die [PidTagAttachDataBinary-Eigenschaft](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) zu finden, die ein binary large object (BLOB) enthält, das den Nachrichtenverlauf für ein #A0 darstellt. 
    
- Lesen Sie dieses Thema, das die Struktur des BLOB beschreibt, und zeigt ein Beispiel-BLOB zum Identifizieren von Nachrichten, die für den Posteingang des POP3-Kontos heruntergeladen oder gelöscht wurden.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a>

## <a name="pop-blob-structure"></a>POP-BLOB-Struktur

Die POP-BLOB-Struktur beginnt, wie in Tabelle 1 beschrieben, mit zwei Feldern, **Version** und **Count,** gefolgt von einer **Anzahl** von Ressourcentags, von denen jedes null-terminated ist. 
  
**Tabelle 1. Struktur des BLOB, das den Nachrichtendownloadverlauf eines POP3-Kontos darstellt**

|**Feld in BLOB**|**Größe**|**Beschreibung**|
|:-----|:-----|:-----|
|**Version** <br/> |2 Bytes  <br/> |Muss 3 sein (**PBLOB_VERSION_NUM**).  <br/> |
|**Count** <br/> |2 Bytes  <br/> |Die Anzahl der Ressourcentags in diesem BLOB.  <br/> |
|Ressourcentag  <br/> |Variable  <br/> |0 oder mehr null-terminierte UTF-8-Zeichenfolgen, die die Ressourcentags codieren. Die Anzahl der mit Null beendeten Zeichenfolgen muss mit **Count übereinstimmen.**  <br/> |
   
Jedes Ressourcentag gibt den Vorgang an, der auf eine Nachricht angewendet wird, einige Datum-Uhrzeit-Metadaten zu dem Vorgang und codiert die UID der Nachricht. Das Format einer Ressourcentagzeichenfolge wird wie folgt aufgeschlüsselt und in Tabelle 2 weiter erläutert. 
  
`Ocyyyymmddhhmmssuuu...`
  
**Tabelle 2. Struktur eines Ressourcentags**

|**Feld in einem Ressourcentag**|**Größe**|**Beschreibung**|
|:-----|:-----|:-----|
| `O` <br/> |1 Zeichen  <br/> |Der Für die E-Mail-Nachricht ausgeführte Vorgang. Der Wert muss "+", "-" oder " sein, was einen erfolgreichen &amp; get-, delete- oder get-and-delete-Vorgang angibt.  <br/> |
| `c` <br/> |1 Zeichen  <br/> |Der Teil des Nachrichteninhalts, der an dem Vorgang beteiligt ist. Der Wert muss " ", "h" oder "b" sein, was den Inhalt von keinem, Header oder Textkörper angibt.  <br/> |
| `yyyy` <br/> |4 Zeichen  <br/> |Das vierstellige Jahr des Vorgangs.  <br/> |
| `MM` <br/> |2 Zeichen  <br/> |Der zweistellige Monat des Vorgangs.  <br/> |
| `dd` <br/> |2 Zeichen  <br/> |Der zweistellige Tag des Vorgangs.  <br/> |
| `hh` <br/> |2 Zeichen  <br/> |Die zweistellige Stunde des Vorgangs.  <br/> |
| `mm` <br/> |2 Zeichen  <br/> |Die zweistellige Minute des Vorgangs.  <br/> |
| `ss` <br/> |2 Zeichen  <br/> |Die zweistellige Sekunde des Vorgangs.  <br/> |
| `uuu…` <br/> |Variable Länge  <br/> |Die codierte UID einer Nachricht.  <br/> |

<a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a>

## <a name="example"></a>Beispiel

Abbildung 1 zeigt ein Beispiel für ein BLOB, das den Nachrichtendownloadverlauf eines POP-Kontos darstellt. 
  
**Abbildung 1. Beispiel-BLOB-Struktur für den Nachrichtendownloadverlauf eines POP3-Kontos**

![BLOB für Nachrichten-Downloadverlauf von POP3-Konto](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
Basierend auf der in Tabelle 1 und Tabelle 2 beschriebenen Struktur stellt dieser BLOB den Downloadverlauf von 23 E-Mail-Nachrichten dar.
  
Beachten Sie zum Analysieren der unformatierten UID in jedem Ressourcentag, dass die UID dieser Codierung folgt: Zeichen in einer UID sind hauptsächlich alphanumerische Zeichen, und jedem nicht alphanumerischen Zeichen wird das ASCII-Zeichen "$" (0x24) vorangehen. Die ASCII-Zeichen $2d stellen also das nicht alphanumerische Zeichen "-" dar. Abbildung 2 zeigt ein Beispiel für das erste Konvertieren der unformatierten UID im Ressourcentag 1 in die ASCII-Darstellung und anschließend das Konvertieren eines nicht alphanumerischen Zeichens, dem "$" vorangegangen ist, um die tatsächliche UID zu erzeugen:
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
**Abbildung 2. Konvertieren der unformatierten UID in einem Ressourcentag in die tatsächliche Nachrichten-UID**

![Konvertieren der Roh-UID in BLOB in tatsächliche Nachrichten-UID](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
Zum Interpretieren von Ressourcentag 1 in diesem BLOB: Die Nachricht mit der UID wurde am  `0BC535DB-EA63-11E1-A75C-00215AD7BB74` 6. September 2012 um 13:11:38 Uhr erfolgreich abgerufen. 
  
Sie können die verbleibenden 22 Ressourcentags für dieses BLOB ähnlich analysieren.
  
## <a name="see-also"></a>Siehe auch
<a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a>

- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md)    
- [Suchen den Nachrichten-Downloadverlauf für ein POP3-Konto](locating-the-message-download-history-for-a-pop3-account.md)    
- [Analyse des POP3-UIDL-Verlaufs](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

