---
title: Analysieren des Nachrichtendownloadverlaufs für ein POP3-Konto
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: In diesem Thema wird die Struktur des POP3-BLOB beschrieben, das den Nachrichtendownloadverlauf eines POP3-Kontos darstellt, um die Nachrichten zu identifizieren, die für dieses Konto heruntergeladen oder gelöscht wurden.
ms.openlocfilehash: d9257c050fa7bd65922aa766b509b7cf0aa60615
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561866"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a>Analysieren des Nachrichtendownloadverlaufs für ein POP3-Konto

In diesem Thema wird die Struktur des POP3-BLOB beschrieben, das den Nachrichtendownloadverlauf eines POP3-Kontos darstellt, um die Nachrichten zu identifizieren, die für dieses Konto heruntergeladen oder gelöscht wurden.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a>

## <a name="why-parse-the-message-download-history"></a>Warum sollte der Nachrichtendownloadverlauf analysiert werden?

Mit dem POP-Anbieter (Post Office Protocol) für Outlook können Benutzer neue E-Mail-Nachrichten auf ihrem lokalen Gerät abrufen und herunterladen und diese E-Mail-Nachrichten anschließend auf dem E-Mail-Server belassen oder löschen. Wenn der E-Mail-Client sucht, dass neue Nachrichten heruntergeladen werden, muss er nur die neuen Nachrichten für diesen Posteingang identifizieren und herunterladen können. Der E-Mail-Client verwendet dazu zuerst den Befehl UIDL (Unique ID Listing), um eine Zuordnung jeder Nachricht abzurufen, die jemals an diesen Posteingang zu einem eindeutigen Bezeichner (UID) übermittelt wurde. Der Client ruft auch den Nachrichtendownloadverlauf für Nachrichten ab, die für den Posteingang auf diesem Client heruntergeladen oder gelöscht wurden. Mithilfe der UID-Zuordnung der Nachricht und des Downloadverlaufs kann der Client dann die Nachrichten, die nicht im Verlauf vorhanden sind, als neu identifizieren und sollten daher heruntergeladen werden.
  
So rufen Sie den Downloadverlauf für Nachrichten für einen Posteingang ab:
  
- Führen Sie die Schritte beim [Suchen des Nachrichtendownloadverlaufs für ein POP3-Konto](locating-the-message-download-history-for-a-pop3-account.md) aus, um nach der [PidTagAttachDataBinary-Eigenschaft](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) zu suchen, die ein BLOB (Binary Large Object) enthält, das den Nachrichtenverlauf für ein POP3-Konto darstellt. 
    
- Lesen Sie dieses Thema, das die Struktur des BLOB beschreibt, und zeigt ein Beispiel-BLOB zum Identifizieren von Nachrichten, die für den Posteingang des POP3-Kontos heruntergeladen oder gelöscht wurden.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a>

## <a name="pop-blob-structure"></a>POP BLOB-Struktur

Die POP BLOB-Struktur, wie in Tabelle 1 beschrieben, beginnt mit zwei Feldern, **Version** und **Anzahl,** gefolgt von einer **Anzahl** von Ressourcentags, von denen jedes null beendet ist. 
  
**Tabelle 1. Struktur des BLOB, das den Nachrichtendownloadverlauf eines POP3-Kontos darstellt**

|**Feld im BLOB**|**Größe**|**Beschreibung**|
|:-----|:-----|:-----|
|**Version** <br/> |2 Bytes  <br/> |Muss 3 (**PBLOB_VERSION_NUM**) sein.  <br/> |
|**Count** <br/> |2 Bytes  <br/> |Die Anzahl der Ressourcentags in diesem BLOB.  <br/> |
|Ressourcentag  <br/> |Variable  <br/> |0 oder mehr mit NULL beendete UTF-8-Zeichenfolgen, die die Ressourcentags codieren. Die Anzahl der Zeichenfolgen, die mit NULL beendet wurden, muss mit **Der Anzahl** übereinstimmen.  <br/> |
   
Jedes Ressourcentag gibt den Vorgang an, der auf eine Nachricht angewendet wird, einige Datum-Uhrzeit-Metadaten zu dem Vorgang und codiert die UID der Nachricht. Das Format einer Ressourcentagzeichenfolge ist wie folgt unterteilt und wird in Tabelle 2 weiter erläutert. 
  
`Ocyyyymmddhhmmssuuu...`
  
**Tabelle 2. Struktur eines Ressourcentags**

|**Feld in einem Ressourcentag**|**Größe**|**Beschreibung**|
|:-----|:-----|:-----|
| `O` <br/> |1 Zeichen  <br/> |Der für die E-Mail-Nachricht ausgeführte Vorgang. Der Wert muss "+", "-" oder " &amp; " sein, was einen erfolgreichen Vorgang zum Abrufen, Löschen oder Abrufen und Löschen angibt.  <br/> |
| `c` <br/> |1 Zeichen  <br/> |Der Teil des Nachrichteninhalts, der an dem Vorgang beteiligt ist. Der Wert muss ", "h" oder "b" sein, was den Inhalt von "none", "header" oder "body" angibt.  <br/> |
| `yyyy` <br/> |4 Zeichen  <br/> |Das vierstellige Jahr des Vorgangs.  <br/> |
| `MM` <br/> |2 Zeichen  <br/> |Der zweiziffrige Monat des Vorgangs.  <br/> |
| `dd` <br/> |2 Zeichen  <br/> |Der zweiziffrige Tag des Vorgangs.  <br/> |
| `hh` <br/> |2 Zeichen  <br/> |Die zweiziffrige Stunde des Vorgangs.  <br/> |
| `mm` <br/> |2 Zeichen  <br/> |Die zweiziffrige Minute des Vorgangs.  <br/> |
| `ss` <br/> |2 Zeichen  <br/> |Die zweiziffrige Sekunde des Vorgangs.  <br/> |
| `uuu…` <br/> |Variable Länge  <br/> |Die codierte UID einer Nachricht.  <br/> |

<a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a>

## <a name="example"></a>Beispiel

Abbildung 1 zeigt ein Beispiel für ein BLOB, das den Nachrichtendownloadverlauf eines POP-Kontos darstellt. 
  
**Abbildung 1. Beispiel-BLOB-Struktur für den Nachrichtendownloadverlauf eines POP3-Kontos**

![BLOB für Nachrichten-Downloadverlauf von POP3-Konto](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
Basierend auf der in Tabelle 1 und Tabelle 2 beschriebenen Struktur stellt dieses BLOB den Downloadverlauf von 23 E-Mail-Nachrichten dar.
  
Um die unformatierte UID in jedem Ressourcentag zu analysieren, beachten Sie, dass die UID dieser Codierung folgt: Zeichen in einer UID sind hauptsächlich alphanumerische Zeichen, und jedem nicht alphanumerischen Zeichen wird das ASCII-Zeichen "$" (0x24) vorangestellt. Die ASCII-Zeichen $2d stellen also das nicht alphanumerische Zeichen "-" dar. Abbildung 2 zeigt ein Beispiel für die erste Konvertierung der unformatierten UID in Ressourcentag 1 in die ASCII-Darstellung und anschließendes Konvertieren eines nicht alphanumerischen Zeichens, dem "$" vorangestellt ist, um die tatsächliche UID zu erzeugen:
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
**Abbildung 2. Konvertieren der unformatierten UID in einem Ressourcentag in die tatsächliche Nachrichten-UID**

![Konvertieren der Roh-UID in BLOB in tatsächliche Nachrichten-UID](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
Um Ressourcentag 1 in diesem BLOB zu interpretieren: Die Nachricht mit der UID  `0BC535DB-EA63-11E1-A75C-00215AD7BB74` wurde am 6. September 2012 um 13:11:38 Uhr erfolgreich abgerufen. 
  
Sie können die verbleibenden 22 Ressourcentags für dieses BLOB auf ähnliche Weise analysieren.
  
## <a name="see-also"></a>Siehe auch
<a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a>

- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md)    
- [Suchen den Nachrichten-Downloadverlauf für ein POP3-Konto](locating-the-message-download-history-for-a-pop3-account.md)    
- [Analysieren des POP3 UIDL-Verlaufs](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

