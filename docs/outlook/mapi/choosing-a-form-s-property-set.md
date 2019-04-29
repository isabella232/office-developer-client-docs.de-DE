---
title: Auswählen eines Formulareigenschaftensatzes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d983b71c7c92c395740a8ae6f6d3666a8bc2c0c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407193"
---
# <a name="choosing-a-forms-property-set"></a>Auswählen eines Formulareigenschaftensatzes

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie Ihren Formularserver implementieren, benötigen Sie eine Eigenschaft für jede Information, die die Nachrichtenklasse benötigt. Diese Eigenschaften können vordefinierte MAPI-Eigenschaften oder benutzerdefinierte Eigenschaften sein, die Sie definieren. Weitere Informationen zum Arbeiten mit Eigenschaften finden Sie unter [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md).
  
Die Formular Konfigurationsdatei enthält eine Liste der Eigenschaften, die der Formularserver für die Verwendung durch Clientanwendungen verfügbar macht, aber dies muss nicht die gesamte Liste von Eigenschaften sein, die von Ihrem Formularserver verwendet werden. Client Anwendungen verwenden in der Regel die verfügbar gemachten Eigenschaften, um Benutzern das Sortieren von Nachrichten in einem Ordner oder das Anpassen ihrer Schnittstellen zu ermöglichen.
  
MAPI verfügt über eine Reihe vordefinierter Eigenschaften, die für die meisten Anwendungen ausreichen. Es kann jedoch vorkommen, dass eine benutzerdefinierte Nachrichtenklasse eine Eigenschaft benötigt, die von MAPI nicht definiert wird. Sie können benutzerdefinierte Eigenschaften verwenden, um den MAPI-vordefinierten Satz von Eigenschaften für alle speziellen Informationen zu erweitern, die der Formularserver unterstützen muss.
  
Sie können eine der folgenden Methoden verwenden, um benutzerdefinierte Eigenschaften zu definieren:
  
- Wählen Sie einen Namen für die Eigenschaft aus, und verwenden Sie die [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode, um ein Property-Tag dafür abzurufen. Die [IMAPIProp](imapipropiunknown.md) -Schnittstelle, über die Sie diese Methode aufrufen, stammt aus dem [IMessage](imessageimapiprop.md) -Zeiger, der beim Erstellen der Nachricht an den Formularserver übergeben wird. Beachten Sie, dass es sich bei dem Eigenschaftsnamen um eine Breitzeichen-Zeichenfolge handeln muss. 
    
- Definieren Sie selbst ein benutzerdefiniertes Property-Tag. Benutzerdefinierte Eigenschaftstags müssen sich im Range 0x6800 bis 0x7BFF befinden. Eigenschaften in diesem Bereichen sind Nachrichtenklassen spezifisch.
    
Weitere Informationen zum Definieren von benutzerdefinierten Eigenschaften finden Sie unter [Definieren neuer MAPI-Eigenschaften](defining-new-mapi-properties.md).
  
> [!NOTE]
> Formularserver mit einem Nachrichtentext verwenden häufig die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft, um Sie zu speichern. Wenn in Ihrem Formularserver **PR_RTF_COMPRESSED**verwendet wird, sollte außerdem sichergestellt werden, dass die **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft eine nur-Text-Version des Nachrichtentexts enthält, falls die resultierende Nachricht von einem Client gelesen wird, der Rich-Text nicht unterstützt. Format (RTF)-Nachrichtentext. 
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln von MAPI-Formular Servern](developing-mapi-form-servers.md)

