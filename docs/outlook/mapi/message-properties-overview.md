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
  
MAPI teilt Nachrichteneigenschaften in drei Typen auf:
  
- Nachrichteninhaltseigenschaften.
    
- Nachrichtenübertragungs- oder Umschlageigenschaften.
    
- Nachrichtenempfängereigenschaften.
    
Nachrichteninhaltseigenschaften beschreiben den Text einer Nachricht. Jede Nachrichtenklasse verfügt über einen eigenen Satz von Inhaltseigenschaften. MAPI definiert Inhaltseigenschaften für Notizen- und Berichtsnachrichten; Die Clients und Nachrichtenspeicheranbieter, die diese Nachrichtenklassen verarbeiten, müssen die Eigenschaften für ihre Implementierungen entsprechend festlegen. **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) sind Beispiele für Inhaltseigenschaften für Notiznachrichten. **PR_BODY** enthält den unformatierten Inhalt einer Notiz, während **PR_RTF_COMPRESSED** die komprimierte Version des formatierten Inhalts einer Notiz enthält. Weitere Informationen zu Eigenschaftenbezeichnerbereichen finden Sie unter [Property Identifier Ranges](property-identifier-ranges.md).
  
Für neue Nachrichtenklassen können Clients inhaltsspezifische Eigenschaften auf zwei Arten definieren:
  
- Mithilfe von Eigenschaftsbezeichnern im Benutzerdefinierten Inhaltseigenschaftenbereich der Nachrichtenklasse: 0x6800 bis 0x7BFF.
    
- Verwenden Sie benannte Eigenschaften mit Bezeichnern, die in den bereich 0x8000 0xFFFE fallen.
    
Der Bezeichnerbereich für benutzerdefinierte Nachrichtenklasseninhaltseigenschaften steht jedem Client zur Verfügung, der eine benutzerdefinierte Nachrichtenklasse erstellt. Daher kann ein Eigenschaftenbezeichner in diesem Bereich für mehrere Nachrichtenklassen verwendet werden. Benutzer von Eigenschaften in diesem Bereich können keine Annahmen zum Verhalten der Eigenschaften treffen. 
  
Für benannte Eigenschaften erstellen Clients einen Namen, der einen Eigenschaftensatz und entweder eine Zeichenzeichenfolge oder einen numerischen Wert für jede neue Eigenschaft angibt. Clients ordnen die Eigenschaft dann einem Bezeichner im benannten Eigenschaftenbereich zu. Benutzer benannter Eigenschaften greifen über die [Methoden IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) nach Name oder Bezeichner darauf zu. 
  
Umschlageigenschaften enthalten Informationen, die zum Übertragen einer Nachricht von einem Empfänger an einen anderen verwendet werden. Wie bei Nachrichteninhaltseigenschaften können Clients oder Dienstanbieter ihre eigenen Umschlageigenschaften definieren, um die von MAPI definierten Zuschläge zu ergänzen. Clients und Transportanbieter legen die Umschlageigenschaften fest, die MAPI basierend auf der definition definiert, die MAPI bietet. Transportanbieter, die spezielle Features implementieren, können eigene Umschlageigenschaften definieren, um diese Features clients zur Verfügung zu stellen. MAPI legt einen Bereich von Eigenschaftenbezeichnern bei, die für diese speziellen vom Anbieter definierten Eigenschaften verwendet werden können. Transportanbieter implementieren in der Regel eine spezielle Eigenschaftenseite, um diese Eigenschaften anzeigen und Clients das Ändern dieser Eigenschaften zu ermöglichen. **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) und **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) sind Beispiele für Umschlageigenschaften. Weitere Informationen finden Sie unter [Property Identifier Ranges](property-identifier-ranges.md).
  
Empfängereigenschaften beschreiben das Ziel einer gesendeten Nachricht. Ein Empfänger kann ein Messagingbenutzer, eine Verteilerliste oder ein Computer sein. Empfängereigenschaften werden von MAPI definiert und von Dienstanbietern festgelegt. Einige Empfängereigenschaften werden von Adressbuchanbietern für ihre Messagingbenutzer- und Verteilerlistenobjekte unterstützt. Andere Empfängereigenschaften werden von Clients, Nachrichtenspeicheranbietern oder Transportanbietern unterstützt. Beispielsweise benötigen alle Empfänger eine Adresse und einen Adresstyp. Dies sind Eigenschaften, die von einem Adressbuchanbieter verwaltet werden, wenn der Empfänger in einem seiner Container gespeichert wird. Empfänger haben auch einen Typ, **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), der einen Empfänger als primären, #A0 oder blinden #A1 identifiziert.
  
Viele Nachrichteneigenschaften sind optional, d. h. Clients können nicht erwarten, dass sie verfügbar sind oder auf gültige Werte festgelegt sind. Einige Nachrichteneigenschaften sind erforderlich, aber nur verfügbar, wenn sich eine Nachricht in einem bestimmten Zustand befindet. Beispielsweise muss eine neu erstellte Nachricht erst nach dem Speichern der Nachricht über einen Eintragsbezeichner verfügen, und es ist nicht erforderlich, eine Nachrichtenklasse zu haben, bis die Nachricht übermittelt werden kann. Clients sollten immer die Ergebnisse ihrer [IMAPIProp::GetProps-](imapiprop-getprops.md) und [IMAPIProp::OpenProperty-Aufrufe](imapiprop-openproperty.md) überprüfen und standardwerte als Sicherung bereit haben, falls eine angeforderte Eigenschaft nicht verfügbar ist. 
  
Die meisten von Dienstanbietern festgelegten Nachrichteneigenschaften sind für Clients schreibgeschützt. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Nachrichten](mapi-messages.md)

