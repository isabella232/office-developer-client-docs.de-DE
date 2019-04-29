---
title: Übersicht über Nachrichteneigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 447f54de-9f0d-4f73-89b6-bed9cfea9c15
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 515b4637f99b806c5c5bc6304f107f62ca6d9091
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420248"
---
# <a name="message-properties-overview"></a>Übersicht über Nachrichteneigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI unterteilt Nachrichteneigenschaften in drei Typen:
  
- Nachrichteninhalts Eigenschaften.
    
- Nachrichtenübermittlung oder Umschlag, Eigenschaften.
    
- Eigenschaften für Nachrichtenempfänger.
    
Nachrichteninhalts Eigenschaften beschreiben den Text einer Nachricht. Jede Nachrichtenklasse verfügt über einen eigenen Satz von Inhaltseigenschaften. MAPI definiert Inhaltseigenschaften für Notiz-und Berichtsnachrichten; die Clients und Nachrichtenspeicher Anbieter, die diese Nachrichtenklassen behandeln, müssen die Eigenschaften entsprechend für Ihre Implementierungen festlegen. **PR_BODY** ([Pidtagbody (](pidtagbody-canonical-property.md)) und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) sind Beispiele für Inhaltseigenschaften für Note-Nachrichten. **PR_BODY** enthält die unformatierten Inhalte einer Note, während **PR_RTF_COMPRESSED** die komprimierte Version des formatierten Inhalts einer Note enthält. Weitere Informationen zu den Bereichen der Eigenschaftsbezeichner finden Sie unter [Eigenschaftenbezeichner Bereiche](property-identifier-ranges.md).
  
Bei neuen Nachrichtenklassen können Clients inhaltsspezifische Eigenschaften auf eine der folgenden Arten definieren:
  
- Durch die Verwendung von Eigenschafts Bezeichnern im Inhalts Eigenschaftenbereich der benutzerdefinierten Nachrichtenklasse: 0x6800 bis 0x7BFF.
    
- Mithilfe benannter Eigenschaften mit Bezeichnern, die in den 0X8000 bis 0xFFFE-Range fallen.
    
Der bezeichnerbereich für benutzerdefinierte Inhaltseigenschaften der Nachrichtenklasse steht jedem Client zur Verfügung, der eine benutzerdefinierte Nachrichtenklasse erstellt. Daher kann ein Eigenschaftenbezeichner in diesem Range für mehrere Nachrichtenklassen verwendet werden. Benutzer von Eigenschaften in diesem Bereichen können keine Annahmen hinsichtlich des Verhaltens der Eigenschaften treffen. 
  
Für benannte Eigenschaften erstellen Clients einen Namen, der einen Eigenschaftensatz und eine Zeichenfolge oder einen numerischen Wert für jede neue Eigenschaft angibt. Clients ordnen die Eigenschaft dann einem Bezeichner im benannten Eigenschaftenbereich zu. Benutzer benannter Eigenschaften greifen über den Namen oder Bezeichner über die Methoden [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) auf Sie zu. 
  
Umschlageigenschaften bieten Informationen, die verwendet werden, um eine Nachricht von einem Empfänger an einen anderen zu übertragen. Wie bei Nachrichteninhalts Eigenschaften können Clients oder Dienstanbieter Ihre eigenen Umschlageigenschaften definieren, um die von MAPI definierten zu ergänzen. Clients und Transportanbieter legen die Umschlageigenschaften fest, die MAPI definiert, basierend auf der Definition, die MAPI bereitstellt. Transport Anbieter, die spezielle Features implementieren, können Ihre eigenen Umschlageigenschaften definieren, um diese Features für Clients verfügbar zu machen. MAPI reserviert eine Reihe von Eigenschaftenbezeichnern, die für diese speziellen Anbieter definierten Eigenschaften verwendet werden können. Transport Anbieter implementieren in der Regel eine spezielle Eigenschaftenseite, um diese Eigenschaften anzuzeigen und Clients zu ermöglichen, diese zu ändern. **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md)) und **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) sind Beispiele für Umschlageigenschaften. Weitere Informationen finden Sie unter [Eigenschaftenbezeichner Bereiche](property-identifier-ranges.md).
  
Empfänger Eigenschaften beschreiben das Ziel für eine gesendete Nachricht. Bei einem Empfänger kann es sich um einen Messagingbenutzer, eine Verteilerliste oder einen Computer handeln. Empfänger Eigenschaften werden durch MAPI definiert und von Dienstanbietern festgelegt. Einige Empfänger Eigenschaften werden von Adressbuch Anbietern für Ihre Messaging-Benutzer-und Verteilerlistenobjekte unterstützt. andere Empfänger Eigenschaften werden von Clients, Nachrichtenspeicher Anbietern oder Transportanbietern unterstützt. Beispielsweise benötigen alle Empfänger eine Adresse und einen Adresstyp; Dabei handelt es sich um Eigenschaften, die von einem Adressbuchanbieter verwaltet werden, wenn der Empfänger in einem seiner Container gespeichert wird. Empfänger haben auch einen Typ, **PR_RECIPIENT_TYPE** ([pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md)), der einen Empfänger als primären, Kohlenstoff Kopien oder blinden Kopie-Empfänger identifiziert.
  
Viele Nachrichteneigenschaften sind optional, was bedeutet, dass Clients nicht erwarten können, dass Sie verfügbar oder auf gültige Werte festgelegt sind. Einige Nachrichteneigenschaften sind erforderlich, sind jedoch nur verfügbar, wenn sich eine Nachricht in einem bestimmten Zustand befindet. Beispielsweise muss eine neu erstellte Nachricht erst dann eine Eintrags-ID haben, nachdem die Nachricht gespeichert wurde, und es ist nicht erforderlich, eine Nachrichtenklasse zu haben, bis die Nachricht zur Übermittlung bereit ist. Clients sollten immer die Ergebnisse ihrer [IMAPIProp::](imapiprop-getprops.md) GetProps und [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Aufrufe überprüfen und Standardwerte als Sicherung bereithalten, falls eine angeforderte Eigenschaft nicht verfügbar ist. 
  
Die meisten Nachrichteneigenschaften, die von Dienstanbietern festgelegt wurden, sind für Clients schreibgeschützt. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Nachrichten](mapi-messages.md)

