---
title: Auswählen eines Formulars Eigenschaftensatz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0ff8d9f1ae25c55d66847b8c0e5e66c406dfdfba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586151"
---
# <a name="choosing-a-forms-property-set"></a>Auswählen eines Formulars Eigenschaftensatz

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wenn Sie Ihr Formular Server implementieren, müssen Sie eine Eigenschaft für jede Informationseinheit befinden, die die Nachrichtenklasse muss. Diese Eigenschaften vordefinierten MAPI-Eigenschaften werden können, oder sie können benutzerdefinierte Eigenschaften, mit denen Sie definiert werden. Weitere Informationen über das Arbeiten mit Eigenschaften finden Sie unter [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md).
  
Die Formular-Konfigurationsdatei enthält eine Liste der Eigenschaften, die für Clientanwendungen mit Ihrem Formular Server verfügbar macht, aber dies ist nicht erforderlich, die gesamte Liste der Eigenschaften, die von Ihrem Formular Server verwendet werden. In der Regel verwenden-Clientanwendungen verfügbar gemachte Eigenschaften, damit Benutzer Nachrichten in einem Ordner sortieren oder ihre Schnittstellen in irgendeiner Weise anpassen.
  
MAPI verfügt über eine Reihe von vordefinierten Eigenschaften, die für die meisten Applikationen ausreichend. Es werden jedoch Zeiten, wenn eine benutzerdefinierte Nachrichtenklasse eine Eigenschaft benötigt, die MAPI nicht definiert. Benutzerdefinierte Eigenschaften können Sie um die MAPI-vordefinierte Gruppe von Eigenschaften für spezielle Informationen zu erweitern, die der Formular Server unterstützen muss.
  
Sie können einen der folgenden Methoden zum Definieren von benutzerdefinierter Eigenschaften verwenden:
  
- Wählen Sie einen Namen für die Eigenschaft, und Verwenden der [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode, um eine Eigenschaftentag zu erhalten. Die [IMAPIProp](imapipropiunknown.md) -Schnittstelle, über die Sie diese Methode aufrufen, stammen aus der [IMessage](imessageimapiprop.md) Zeiger, der mit dem Formular Server übergeben wird, wenn die Nachricht erstellt wird. Beachten Sie, dass der Name der Eigenschaft eine Zeichenfolge mit Breitzeichen sein muss. 
    
- Definieren einer benutzerdefinierten Eigenschaftentag selbst. Eigenschaftentags-benutzerdefinierte muss im Bereich 0x6800 bis 0x7BFF. Eigenschaften in diesem Bereich sind Nachrichtenklasse spezifische.
    
Weitere Informationen zum Definieren von benutzerdefinierter Eigenschaften finden Sie unter [Definieren eines neuen MAPI-Eigenschaften](defining-new-mapi-properties.md).
  
> [!NOTE]
> Formular Server, auf denen einen Nachrichtentext häufig verwenden Sie die Eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) speichern. Wenn Ihr Formular Server **PR_RTF_COMPRESSED**verwendet, sollten sie außerdem sicherstellen, dass die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft eine nur-Text-Version von den Nachrichtentext enthält für den Fall, dass die resultierende Nachricht von einem Client gelesen wird, der Rich-Text nicht unterstützt Nachrichtentext-Format (RTF). 
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

