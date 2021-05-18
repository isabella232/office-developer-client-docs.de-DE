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
  
Wenn Sie den Formularserver implementieren, benötigen Sie eine Eigenschaft für alle Informationen, die Ihre Nachrichtenklasse benötigt. Diese Eigenschaften können vordefinierte MAPI-Eigenschaften oder benutzerdefinierte Eigenschaften sein, die Sie definieren. Weitere Informationen zum Arbeiten mit Eigenschaften finden Sie unter [MAPI Property Overview](mapi-property-overview.md).
  
Die Formularkonfigurationsdatei enthält eine Liste der Eigenschaften, die ihr Formularserver für die Verwendung von Clientanwendungen verfügbar macht. Dies muss jedoch nicht die gesamte Liste der vom Formularserver verwendeten Eigenschaften sein. Clientanwendungen verwenden in der Regel die verfügbar gemachten Eigenschaften, damit Benutzer Nachrichten in einem Ordner sortieren oder ihre Schnittstellen auf irgendeine Weise anpassen können.
  
MAPI verfügt über einen großen Satz vordefinierter Eigenschaften, die für die meisten Anwendungen ausreichen. Es kommt jedoch vor, dass eine benutzerdefinierte Nachrichtenklasse eine Eigenschaft benötigt, die MAPI nicht definiert. Sie können benutzerdefinierte Eigenschaften verwenden, um den vordefinierten MapI-Eigenschaftensatz für alle speziellen Informationen zu erweitern, die ihr Formularserver unterstützen muss.
  
Sie können eine der folgenden Methoden verwenden, um benutzerdefinierte Eigenschaften zu definieren:
  
- Wählen Sie einen Namen für die Eigenschaft aus, und verwenden Sie die [IMAPIProp::GetIDsFromNames-Methode,](imapiprop-getidsfromnames.md) um ein Eigenschaftstag dafür zu erhalten. Die [IMAPIProp-Schnittstelle,](imapipropiunknown.md) über die Sie diese Methode aufrufen, stammt vom [IMessage-Zeiger,](imessageimapiprop.md) der beim Erstellen der Nachricht an den Formularserver übergeben wird. Beachten Sie, dass der Eigenschaftenname eine Zeichenfolge mit breitem Zeichen sein muss. 
    
- Definieren Sie selbst ein benutzerdefiniertes Eigenschaftentag. Benutzerdefinierte Eigenschaftstags müssen sich im Bereich von 0x6800 bis 0x7BFF. Eigenschaften in diesem Bereich sind nachrichtenklassenspezifisch.
    
Weitere Informationen zum Definieren benutzerdefinierter Eigenschaften finden Sie unter [Defining New MAPI Properties](defining-new-mapi-properties.md).
  
> [!NOTE]
> Formularserver mit einem Nachrichtentext verwenden häufig die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) -Eigenschaft, um sie zu speichern. Wenn ihr Formularserver **PR_RTF_COMPRESSED** verwendet, sollte er auch sicherstellen, dass die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft eine text only-Version des Nachrichtentexts enthält, falls die resultierende Nachricht von einem Client gelesen wird, der #A0 (Rich Text Format) nicht unterstützt. 
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

