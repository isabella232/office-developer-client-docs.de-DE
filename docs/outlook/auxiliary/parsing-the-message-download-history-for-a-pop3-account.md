---
title: Analysieren des Nachrichtendownloadverlaufs für ein POP3-Konto
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: In diesem Thema wird die Struktur des POP3-BLOBs beschrieben, die den Nachrichten Downloadverlauf eines POP3-Kontos darstellt, um die Nachrichten zu identifizieren, die in diesem Konto heruntergeladen oder gelöscht wurden.
ms.openlocfilehash: 44a799f6b6fbe2a2841522c18405149a470b0236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327763"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a>Analysieren des Nachrichtendownloadverlaufs für ein POP3-Konto

In diesem Thema wird die Struktur des POP3-BLOBs beschrieben, die den Nachrichten Downloadverlauf eines POP3-Kontos darstellt, um die Nachrichten zu identifizieren, die in diesem Konto heruntergeladen oder gelöscht wurden.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a>

## <a name="why-parse-the-message-download-history"></a>Warum sollte der Nachrichten Downloadverlauf analysiert werden?

Der POP-Anbieter (Post Office Protocol) für Outlook ermöglicht Benutzern das Abrufen und Herunterladen neuer e-Mail-Nachrichten auf dem lokalen Gerät und das anschließende verlassen oder Löschen dieser e-Mail-Nachrichten auf dem e-Mail-Server. Wenn der e-Mail-Client prüft, ob neue Nachrichten heruntergeladen werden sollen, muss er nur die neuen Nachrichten für diesen Posteingang identifizieren und herunterladen können. Der e-Mail-Client verwendet dies zunächst mit dem Befehl UIDL (Unique ID Listing), um eine Karte jeder Nachricht zu erhalten, die jemals an diesen Posteingang an einen eindeutigen Bezeichner (UID) übermittelt wurde. Der Client ruft auch den Nachrichten Downloadverlauf für Nachrichten ab, die heruntergeladen oder für den Posteingang auf diesem Client gelöscht wurden. Mithilfe der Nachrichten-UID-Zuordnung und des downloadverlaufs kann der Client die Nachrichten identifizieren, die aus dem Verlauf als neu abwesend sind und daher heruntergeladen werden sollten.
  
So rufen Sie den Nachrichten-Downloadverlauf für einen Posteingang ab
  
- Führen Sie die Schritte unter [Suchen des Nachrichten downloadverlaufs für ein POP3-Konto](locating-the-message-download-history-for-a-pop3-account.md) aus, um die [pidtagattachdatabinary (](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) -Eigenschaft zu finden, die ein BLOB (Binary Large Object) enthält, das den Nachrichtenverlauf für ein POP3-Konto darstellt. 
    
- Lesen Sie dieses Thema, in dem die Struktur des BLOBs beschrieben wird, und zeigen Sie ein Beispiel-BLOB an, um Nachrichten zu identifizieren, die heruntergeladen oder für den Posteingang des POP3-Kontos gelöscht wurden.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a>

## <a name="pop-blob-structure"></a>POP-BLOB-Struktur

Die POP-BLOB-Struktur, wie in Tabelle 1 beschrieben, beginnt mit zwei Feldern, **Version** und **Anzahl**, gefolgt **** von einer Anzahl von Ressourcen Tags, die jeweils NULL-terminiert sind. 
  
**Tabelle 1. Struktur des BLOBs, die den Nachrichten Downloadverlauf eines POP3-Kontos darstellt**

|**Feld in BLOB**|**Size**|**Beschreibung**|
|:-----|:-----|:-----|
|**Version** <br/> |2 Byte  <br/> |Muss 3 (**PBLOB_VERSION_NUM**) sein.  <br/> |
|**Count** <br/> |2 Byte  <br/> |Die Anzahl der Ressourcen Tags in diesem BLOB.  <br/> |
|Ressourcentag  <br/> |Variable  <br/> |0 oder mehr Null-terminierte UTF-8-Zeichenfolgen, die die Ressourcen Tags codieren. Die Anzahl der null-terminierten Zeichenfolgen muss mit **count**übereinstimmen.  <br/> |
   
Jedes Resource-Tag gibt den Vorgang an, der auf eine Nachricht angewendet wird, einige Datum-Zeit-Metadaten über den Vorgang und codiert die UID der Nachricht. Das Format einer Resource-Tag-Zeichenfolge wird wie folgt aufgeschlüsselt und wird in Tabelle 2 weiter erläutert. 
  
`Ocyyyymmddhhmmssuuu...`
  
**Tabelle 2. Struktur eines Ressourcen Tags**

|**Feld in einem ressourcentag**|**Size**|**Beschreibung**|
|:-----|:-----|:-----|
| `O` <br/> |1 Zeichen  <br/> |Der Vorgang, der für die e-Mail-Nachricht ausgeführt wird. Der Wert muss "+", "-" oder "&amp;" sein, wodurch ein erfolgreicher Get-, DELETE-oder Get-and-Delete-Vorgang angegeben wird.  <br/> |
| `c` <br/> |1 Zeichen  <br/> |Der Teil des Nachrichteninhalts, der an dem Vorgang beteiligt ist. Der Wert muss "", "h" oder "b" sein, der den Inhalt von None, Header oder Body angibt.  <br/> |
| `yyyy` <br/> |4 Zeichen  <br/> |Das vierstellige Jahr des Vorgangs.  <br/> |
| `MM` <br/> |2 Zeichen  <br/> |Der zweistellige Monat des Vorgangs.  <br/> |
| `dd` <br/> |2 Zeichen  <br/> |Der zweistellige Tag des Vorgangs.  <br/> |
| `hh` <br/> |2 Zeichen  <br/> |Die zweistellige Stunde des Vorgangs.  <br/> |
| `mm` <br/> |2 Zeichen  <br/> |Die zweistellige Minute des Vorgangs.  <br/> |
| `ss` <br/> |2 Zeichen  <br/> |Die zweistellige Sekunde des Vorgangs.  <br/> |
| `uuu…` <br/> |Variable Länge  <br/> |Die codierte UID einer Nachricht.  <br/> |

<a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a>

## <a name="example"></a>Beispiel

Abbildung 1 zeigt ein Beispiel für ein BLOB, das den Nachrichten Downloadverlauf eines POP-Kontos darstellt. 
  
**Abbildung 1. Beispiel einer BLOB-Struktur für den Nachrichten Downloadverlauf eines POP3-Kontos**

![BLOB für Nachrichten-Downloadverlauf von POP3-Konto](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
Basierend auf der in Tabelle 1 und Tabelle 2 beschriebenen Struktur stellt dieses BLOB den Downloadverlauf von 23 e-Mail-Nachrichten dar.
  
Wenn Sie die RAW-UID in jedem Resource-Tag analysieren möchten, beachten Sie, dass die UID dieser Codierung folgt: die Zeichen in einer UID sind meist alphanumerische Zeichen, und jedem nicht alphanumerischen Zeichen wird das ASCII-Zeichen "$" vorangestellt (0x24). Die ASCII-Zeichen $2D stellen also das nicht alphanumerische Zeichen "-" dar. Abbildung 2 zeigt ein Beispiel für die erste Konvertierung der rohen UID in Resource Tag 1 in die ASCII-Darstellung und dann die Konvertierung von einem nicht-alphanumerischem Zeichen vorangestellt von "$", um die tatsächliche UID zu erzeugen:
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
**Abbildung 2. Konvertieren der rohen UID in einem Resource-Tag in die tatsächliche Nachrichten-UID**

![Konvertieren der Roh-UID in BLOB in tatsächliche Nachrichten-UID](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
So interpretieren Sie Resource Tag 1 in diesem BLOB: die Nachricht mit der `0BC535DB-EA63-11E1-A75C-00215AD7BB74` UID wurde am 6. September 2012 um 13:11:38 erfolgreich abgerufen. 
  
Sie können auch die restlichen 22 Ressourcen Tags für diesen BLOB analysieren.
  
## <a name="see-also"></a>Siehe auch
<a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a>

- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md)    
- [Suchen den Nachrichten-Downloadverlauf für ein POP3-Konto](locating-the-message-download-history-for-a-pop3-account.md)    
- [Analysieren des POP3-UIDL-Verlaufs](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

