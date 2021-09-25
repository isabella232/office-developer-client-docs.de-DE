---
title: Übersicht über Nachrichteneigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 447f54de-9f0d-4f73-89b6-bed9cfea9c15
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b934a4d431cb9958fb594eba2ab13d27db4c413e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551121"
---
# <a name="message-properties-overview"></a>Übersicht über Nachrichteneigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI unterteilt Nachrichteneigenschaften in drei Typen:
  
- Nachrichteninhaltseigenschaften.
    
- Nachrichtenübertragungs- oder Umschlageigenschaften.
    
- Nachrichtenempfängereigenschaften.
    
Nachrichteninhaltseigenschaften beschreiben den Text einer Nachricht. Jede Nachrichtenklasse verfügt über einen eigenen Satz von Inhaltseigenschaften. MAPI definiert Inhaltseigenschaften für Notiz- und Berichtsnachrichten. Es liegt an den Clients und Nachrichtenspeicheranbietern, die diese Klassen von Nachrichten behandeln, die Eigenschaften für ihre Implementierungen entsprechend festzulegen. **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) sind Beispiele für Inhaltseigenschaften für Notizmeldungen. **PR_BODY** enthält den unformatierten Inhalt einer Notiz, **während PR_RTF_COMPRESSED** die komprimierte Version des formatierten Inhalts einer Notiz enthält. Weitere Informationen zu Eigenschaftsbezeichnerbereichen finden Sie unter [Eigenschaftenbezeichnerbereiche.](property-identifier-ranges.md)
  
Für neue Nachrichtenklassen können Clients inhaltsspezifische Eigenschaften auf zwei Arten definieren:
  
- Mithilfe von Eigenschaftsbezeichnern im Eigenschaftenbereich der benutzerdefinierten Nachrichtenklasse: 0x6800 bis 0x7BFF.
    
- Mithilfe von benannten Eigenschaften mit Bezeichnern, die in den 0x8000 bis 0xFFFE Bereich fallen.
    
Der Bezeichnerbereich für benutzerdefinierte Nachrichtenklassen-Inhaltseigenschaften ist für jeden Client verfügbar, der eine benutzerdefinierte Nachrichtenklasse erstellt. Daher kann ein Eigenschaftsbezeichner in diesem Bereich für mehrere Nachrichtenklassen verwendet werden. Benutzer von Eigenschaften in diesem Bereich können nicht vom Verhalten der Eigenschaften ausgehen. 
  
Für benannte Eigenschaften erstellen Clients einen Namen, der einen Eigenschaftensatz und entweder eine Zeichenfolge oder einen numerischen Wert für jede neue Eigenschaft angibt. Clients ordnen die Eigenschaft dann einem Bezeichner im benannten Eigenschaftenbereich zu. Benutzer benannter Eigenschaften greifen über die Methoden [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) auf sie über den Namen oder bezeichner zu. 
  
Briefumschlageigenschaften stellen Informationen bereit, die verwendet werden, um eine Nachricht von einem Empfänger an einen anderen zu übertragen. Wie bei Nachrichteninhaltseigenschaften ist es für Clients oder Dienstanbieter möglich, ihre eigenen Briefumschlageigenschaften zu definieren, um die von mapi definierten Eigenschaften zu ergänzen. Clients und Transportanbieter legen die Briefumschlageigenschaften fest, die mapi basierend auf der von mapi bereitgestellten Definition definiert. Transportanbieter, die spezielle Features implementieren, können ihre eigenen Briefumschlageigenschaften definieren, um diese Features für Clients verfügbar zu machen. MAPI reserviert einen Bereich von Eigenschaftsbezeichnern, die für diese speziellen vom Anbieter definierten Eigenschaften verwendet werden können. Transportanbieter implementieren in der Regel eine spezielle Eigenschaftenseite, um diese Eigenschaften anzuzeigen und es Clients zu ermöglichen, sie zu ändern. **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) und **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) sind Beispiele für Umschlageigenschaften. Weitere Informationen finden Sie unter [Eigenschaftenbezeichnerbereiche.](property-identifier-ranges.md)
  
Empfängereigenschaften beschreiben das Ziel einer gesendeten Nachricht. Ein Empfänger kann ein Messagingbenutzer, eine Verteilerliste oder ein Computer sein. Empfängereigenschaften werden von MAPI definiert und von Dienstanbietern festgelegt. Einige Empfängereigenschaften werden von Adressbuchanbietern für ihre Nachrichtenbenutzer- und Verteilerlistenobjekte unterstützt. andere Empfängereigenschaften werden von Clients, Nachrichtenspeicheranbietern oder Transportanbietern unterstützt. Beispielsweise benötigen alle Empfänger eine Adresse und einen Adresstyp. Dies sind Eigenschaften, die von einem Adressbuchanbieter verwaltet werden, wenn der Empfänger in einem seiner Container gespeichert wird. Empfänger haben auch den Typ **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), der einen Empfänger als primären Empfänger, Kopierkopie oder Blindkopieempfänger identifiziert.
  
Viele Nachrichteneigenschaften sind optional, was bedeutet, dass Clients nicht erwarten können, dass sie verfügbar sind oder auf gültige Werte festgelegt sind. Einige Nachrichteneigenschaften sind erforderlich, aber nur verfügbar, wenn sich eine Nachricht in einem bestimmten Zustand befindet. Beispielsweise muss eine neu erstellte Nachricht erst nach dem Speichern der Nachricht über einen Eintragsbezeichner verfügen, und es ist nicht erforderlich, eine Nachrichtenklasse zu haben, bis die Nachricht gesendet werden kann. Clients sollten immer die Ergebnisse ihrer [IMAPIProp::GetProps-](imapiprop-getprops.md) und [IMAPIProp::OpenProperty-Aufrufe](imapiprop-openproperty.md) überprüfen und Standardwerte als Sicherung bereit halten, falls eine angeforderte Eigenschaft nicht verfügbar ist. 
  
Die meisten Nachrichteneigenschaften, die Dienstanbieter festlegen, sind für Clients schreibgeschützt. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Nachrichten](mapi-messages.md)

