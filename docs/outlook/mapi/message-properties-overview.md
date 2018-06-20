---
title: Nachricht Eigenschaften (Übersicht)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 447f54de-9f0d-4f73-89b6-bed9cfea9c15
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 78e2f63746a866603bc2392fbe5c8bb25d3f38c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793264"
---
# <a name="message-properties-overview"></a>Nachricht Eigenschaften (Übersicht)

  
  
**Betrifft**: Outlook 
  
MAPI ist Nachrichteneigenschaften in drei Typen unterteilt:
  
- Content Nachrichteneigenschaften.
    
- Nachrichteneigenschaften Übertragung, oder einen Umschlag zu.
    
- Nachricht Empfängereigenschaften.
    
Content Nachrichteneigenschaften beschreiben den Text einer Nachricht. Jede Nachrichtenklasse verfügt über einen eigenen Satz an Content-Eigenschaften. MAPI definiert Content-Eigenschaften für Notizen und Bericht Nachrichten. Es ist bis zu Clients and Message-Anbieter, die diese Klassen werden Nachrichten an die Eigenschaften entsprechend ihren Implementierungen festlegen behandelt. **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) sind Beispiele für Content-Eigenschaften für Hinweis Nachrichten. **PR_BODY** enthält den unformatierten Inhalt einer Notiz **PR_RTF_COMPRESSED** die komprimierte Version der formatierte Inhalt einer Notiz. Weitere Informationen zur Eigenschaft Bezeichner Bereichen finden Sie unter [Eigenschaft Bezeichner Bereiche](property-identifier-ranges.md).
  
Für neue Nachrichtenklassen; können Clients in einem der folgenden beiden Methoden Inhalte-spezifische Eigenschaften definieren:
  
- Im Bereich benutzerdefinierten Meldung Klasse-Content-Eigenschaften mithilfe von Eigenschaftenbezeichner: 0x6800 über 0x7BFF.
    
- Mithilfe von benannten Eigenschaften mit IDs, die in der 0 x 8000 über 0xFFFE Bereich liegen.
    
Der Bezeichner Bereich für benutzerdefinierte Meldung Klasseneigenschaften Content steht jeder Client, der eine benutzerdefinierte Nachrichtenklasse erstellt. Aus diesem Grund kann ein Bezeichner in diesem Bereich für mehrere Nachrichtenklassen verwendet werden. Benutzer von Eigenschaften in diesem Bereich Annahmen über das Verhalten der Eigenschaften nicht möglich. 
  
Clients erstellen für benannte Eigenschaften einen Namen, der einen Eigenschaftensatz und eine Zeichenfolge oder einen numerischen Wert für jede neue Eigenschaft angibt. Clients ordnen Sie dann die-Eigenschaft einen Bezeichner in der benannten Eigenschaftsbereich. Benutzer von benannten Eigenschaften, die sie durch den Namen oder Bezeichner über die Methoden [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) zugreifen. 
  
Umschlageigenschaften enthalten Informationen, die verwendet wird, um eine Nachricht von einem Empfänger in eine andere zu übertragen. Wie bei Content Nachrichteneigenschaften, ist es möglich, dass Clients oder Dienstanbieter eigene Umschlageigenschaften definieren, die zu ergänzen, die MAPI definiert. Clients und Transportanbieter Umschlageigenschaften festlegen, die MAPI definiert basierend auf der Definition, die MAPI bietet. Transportanbieter, die spezielle Features implementieren können ihre eigenen Umschlageigenschaften, um die Features für Clients verfügbar machen definieren. MAPI reserviert einen Bereich von eigenschaftskennungen, die für diese speziellen vom Anbieter definiertes Eigenschaften verwendet werden können. Transportanbieter implementieren in der Regel eine spezielle Eigenschaftenseite um diese Eigenschaften anzuzeigen, und Aktivieren von Clients, sie zu ändern. **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) und **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) sind Beispiele für Eigenschaften von Umschlägen. Weitere Informationen finden Sie unter [Eigenschaft Bezeichner Bereiche](property-identifier-ranges.md).
  
Empfängereigenschaften beschreiben das Ziel für eine gesendete Nachricht. Ein Empfänger kann ein messaging-Benutzer, Verteilerliste oder einem Computer sein. Empfängereigenschaften werden von MAPI definierten und vom Dienstanbieter festgelegt. Einige Empfängereigenschaften werden von adressbuchanbietern implementierte für ihre messaging-Benutzer und Verteilung List-Objekten unterstützt. andere Empfängereigenschaften werden von Clients, Nachricht Store oder Transportanbieter unterstützt. Beispielsweise erfordern alle Empfänger eine Adresse und einen Adresstyp. Dies sind die Eigenschaften, die vom Adressbuch-Dienstanbieter verwaltet werden, wenn der Empfänger in einem von den Containern gespeichert ist. Empfänger können auch einen Typ, **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), die einen Empfänger als Primär, Carbon Copy, Blindkopie oder Bcc-Empfänger identifiziert.
  
Viele Nachrichteneigenschaften sind optional, d. h., dass Clients verfügbar oder festgelegten erwartet können nicht auf gültige Werte. Einige Nachrichteneigenschaften sind erforderlich, aber verfügbar, nur, wenn eine Nachricht in einem bestimmten Zustand befindet. Eine neu erstellte Nachricht ist beispielsweise nicht erforderlich, um einen Eintrag Bezeichner bis haben, nachdem die Nachricht wurde gespeichert, und es nicht erforderlich ist, um eine Nachrichtenklasse haben, bis die Nachricht gesendet werden kann. Clients sollte immer überprüfen Sie die Ergebnisse der ihre Anrufe [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPIProp::OpenProperty](imapiprop-openproperty.md) und haben die Standardwerte bereit als Sicherung für den Fall, dass eine angeforderte Eigenschaft nicht verfügbar ist. 
  
Die meisten Nachrichteneigenschaften, die Dienstanbieter festgelegt sind, an die Clients schreibgeschützt. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Nachrichten](mapi-messages.md)

