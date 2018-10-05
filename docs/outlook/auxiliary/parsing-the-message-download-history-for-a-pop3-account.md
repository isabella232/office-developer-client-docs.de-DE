---
title: Analysieren des Nachrichtendownloadverlaufs für ein POP3-Konto
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: In diesem Thema wird die Struktur des POP3-BLOBs, die den Nachricht Downloadverlauf von POP3-Konto zur Kennzeichnung der Nachrichten, die auf dieses Konto gelöscht oder heruntergeladen wurden darstellt.
ms.openlocfilehash: 44a799f6b6fbe2a2841522c18405149a470b0236
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389008"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a>Analysieren des Nachrichtendownloadverlaufs für ein POP3-Konto

In diesem Thema wird die Struktur des POP3-BLOBs, die den Nachricht Downloadverlauf von POP3-Konto zur Kennzeichnung der Nachrichten, die auf dieses Konto gelöscht oder heruntergeladen wurden darstellt.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a>

## <a name="why-parse-the-message-download-history"></a>Warum Analysieren des Nachrichtenverlaufs herunterladen?

Der Anbieter Post Office Protocol (POP) für Outlook ermöglicht Benutzern abgerufen, und Laden Sie neue e-Mail-Nachrichten auf ihrem lokalen Gerät, und anschließend lassen oder löschen diese e-Mail-Nachrichten auf dem e-Mail-Server. E-Mail-Client für neue Nachrichten herunterladen überprüft, verfügt zu identifizieren, und Laden Sie nur die neuen Nachrichten für Posteingang. E-Mail-Client wird mithilfe der ersten den Befehl UIDL (eindeutige ID auflisten) eine Zuordnung der einzelnen Nachrichten abrufen, die jemals an Posteingang auf einen eindeutigen Bezeichner (UID) übermittelt wurde. Der Client ruft auch den Nachrichten-Downloadverlauf für Nachrichten, die heruntergeladen oder für den Posteingang auf den Client gelöscht wurden. Mit der Meldung UID-Karte und Downloadverlauf, Identifizieren des Clients kann dann diese Nachrichten, die nicht vorhanden sind von den Verlauf als neue und somit, heruntergeladen werden soll.
  
Um die Nachrichten Downloadverlauf für ein Posteingang zu erhalten:
  
- Führen Sie die Schritte in [die Nachricht suchen Downloadverlauf für ein POP3-Konto](locating-the-message-download-history-for-a-pop3-account.md) , die Eigenschaft [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) zu erhalten, die ein binary large Object (BLOB) enthält, die für ein POP3-Konto des Nachrichtenverlaufs darstellt. 
    
- Lesen Sie dieses Thema, das beschreibt der Struktur des BLOB, und zeigt ein Beispiel für BLOB zur Identifikation von Nachrichten, die heruntergeladen oder für den Posteingang von POP3-Konto gelöscht wurden.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a>

## <a name="pop-blob-structure"></a>POP BLOB-Struktur

Die POP-BLOB-Struktur beginnt wie in Tabelle 1 beschrieben mit zwei Feldern, **Version** und **Count**, gefolgt von einem **Count** Anzahl von Resource-Tags, von die jedes Null endende ist. 
  
**In Tabelle 1. Struktur des BLOBs, die Meldung darstellt, Downloadverlauf von POP3-Konto**

|**Feld in BLOB**|**Size**|**Beschreibung**|
|:-----|:-----|:-----|
|**Version** <br/> |2 Bytes  <br/> |Muss 3 (**PBLOB_VERSION_NUM**).  <br/> |
|**Count** <br/> |2 Bytes  <br/> |Die Nummer der Ressource in dieses BLOB-tags.  <br/> |
|Resource-tag  <br/> |Variable  <br/> |0 oder mehr Null endende UTF-8-Zeichenfolgen, die die Ressource Tags codiert. Die Anzahl der Zeichenfolgen mit Null endende muss **Count**übereinstimmen.  <br/> |
   
Jede Ressource-Tag gibt den Vorgang, der die UID der Nachricht codiert und auf einigen Datum-/ Uhrzeit-Metadaten, die über den Vorgang, eine Nachricht angewendet wird. Das Format einer Ressource Tag Zeichenfolge wie folgt aufgeschlüsselt und wird in Tabelle 2 ausführlich erläutert. 
  
`Ocyyyymmddhhmmssuuu...`
  
**In Tabelle 2. Struktur eines Resource-Tags**

|**Feld in einem Tag Ressource**|**Size**|**Beschreibung**|
|:-----|:-----|:-----|
| `O` <br/> |1 Zeichen  <br/> |Die Operation, die für die e-Mail-Nachricht durchgeführt werden. Der Wert muss "+" und "-", oder "&amp;", die eine erfolgreiche Get, löschen oder Get-und-Löschvorgang jeweils angibt.  <br/> |
| `c` <br/> |1 Zeichen  <br/> |Der Teil der Inhalt der Nachricht beteiligt sind. Der Wert muss "", "h" oder "b", die den Inhalt des none gibt an, Kopf- oder Body, jeweils.  <br/> |
| `yyyy` <br/> |4 Zeichen  <br/> |Die vierstellige Jahresangabe des Vorgangs.  <br/> |
| `MM` <br/> |2 Zeichen  <br/> |Der zweistelligen Monat des Vorgangs.  <br/> |
| `dd` <br/> |2 Zeichen  <br/> |Die zweistellige Angabe des Tags des Vorgangs.  <br/> |
| `hh` <br/> |2 Zeichen  <br/> |Die zweistellige Stunde des Vorgangs.  <br/> |
| `mm` <br/> |2 Zeichen  <br/> |Die Minutenangabe des Vorgangs.  <br/> |
| `ss` <br/> |2 Zeichen  <br/> |Die zweite zweistellige Angabe des Vorgangs.  <br/> |
| `uuu…` <br/> |Variabler Länge  <br/> |Die codierte UID einer Nachricht.  <br/> |

<a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a>

## <a name="example"></a>Beispiel

Abbildung 1 zeigt ein Beispiel für ein BLOB, den Nachricht Downloadverlauf für ein POP-Konto darstellt. 
  
**Abbildung 1. Beispiel BLOB-Struktur für die Nachricht Downloadverlauf von POP3-Konto**

![BLOB für Nachrichten-Downloadverlauf von POP3-Konto](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
Basierend auf der Struktur, die in Tabelle 1 und Tabelle 2 beschrieben, stellt diese BLOB den Downloadverlauf 23 e-Mail-Nachrichten.
  
Zum Analysieren der rohen-UID in jeder Ressource Tag, beachten Sie, dass die UID diese Codierung erfolgt: Zeichen in einer UID sind größtenteils alphanumerischen Zeichen, und jedes nicht alphanumerische Zeichen vor dem ASCII-Zeichen "$" (0 x 24). Damit die ASCII 2d darstellen, die nicht alphanumerische Zeichen $ Zeichen "-". Abbildung 2 zeigt ein Beispiel für die zunächst auf die Darstellung von ASCII-Konvertieren der rohen-UID in Ressource Tag 1, und klicken Sie dann konvertieren von einem nicht alphanumerische Zeichen vorangestellt "$", um die tatsächliche UID zu erstellen:
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
**Abbildung 2. Konvertieren der rohen-UID in einem Tag Ressource in die tatsächliche Nachrichten-UID**

![Konvertieren der Roh-UID in BLOB in tatsächliche Nachrichten-UID](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
Interpretieren der Ressource in dieses BLOB-Tag 1: die Nachricht mit der UID `0BC535DB-EA63-11E1-A75C-00215AD7BB74` erfolgreich 6 September 2012 unter 13:11:38 abgerufen wurde. 
  
Sie können auf ähnliche Weise die verbleibenden 22 Ressource Tags für dieses BLOB analysieren.
  
## <a name="see-also"></a>Siehe auch
<a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a>

- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md)    
- [Suchen den Nachrichten-Downloadverlauf für ein POP3-Konto](locating-the-message-download-history-for-a-pop3-account.md)    
- [Analysieren des POP3 UIDL-Verlaufs](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

