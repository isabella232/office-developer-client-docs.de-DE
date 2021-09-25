---
title: Auswählen eines Formulareigenschaftensatzes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b18ac45fe04f1e299199e4a51bf952856d5bd85d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584724"
---
# <a name="choosing-a-forms-property-set"></a>Auswählen eines Formulareigenschaftensatzes

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie den Formularserver implementieren, benötigen Sie eine Eigenschaft für jede Information, die ihre Nachrichtenklasse benötigt. Diese Eigenschaften können vordefinierte MAPI-Eigenschaften oder benutzerdefinierte Eigenschaften sein, die Sie definieren. Weitere Informationen zum Arbeiten mit Eigenschaften finden Sie unter [MAPI Property Overview](mapi-property-overview.md).
  
Die Formularkonfigurationsdatei enthält eine Liste der Eigenschaften, die der Formularserver für die Verwendung durch Clientanwendungen verfügbar macht. Dies muss jedoch nicht die gesamte Liste der eigenschaften sein, die vom Formularserver verwendet werden. Clientanwendungen verwenden in der Regel die verfügbar gemachten Eigenschaften, um Es Benutzern zu ermöglichen, Nachrichten in einem Ordner zu sortieren oder ihre Schnittstellen auf irgendeine Weise anzupassen.
  
DIE MAPI verfügt über einen großen Satz vordefinierter Eigenschaften, die für die meisten Anwendungen ausreichen. Es gibt jedoch Situationen, in denen eine benutzerdefinierte Nachrichtenklasse eine Eigenschaft benötigt, die mapi nicht definiert. Sie können benutzerdefinierte Eigenschaften verwenden, um den vordefinierten MAPI-Eigenschaftensatz für alle speziellen Informationen zu erweitern, die der Formularserver unterstützen muss.
  
Sie können eine der folgenden Methoden verwenden, um benutzerdefinierte Eigenschaften zu definieren:
  
- Wählen Sie einen Namen für die Eigenschaft aus, und verwenden Sie die [IMAPIProp::GetIDsFromNames-Methode,](imapiprop-getidsfromnames.md) um ein Eigenschaftstag dafür abzurufen. Die [IMAPIProp-Schnittstelle,](imapipropiunknown.md) über die Sie diese Methode aufrufen, stammt aus dem [IMessage-Zeiger,](imessageimapiprop.md) der beim Erstellen der Nachricht an den Formularserver übergeben wird. Beachten Sie, dass der Eigenschaftenname eine zeichenfolge mit breitem Zeichen sein muss. 
    
- Definieren Sie selbst ein benutzerdefiniertes Eigenschaftentag. Benutzerdefinierte Eigenschaftentags müssen sich im Bereich 0x6800 bis 0x7BFF befinden. Eigenschaften in diesem Bereich sind nachrichtenklassenspezifisch.
    
Weitere Informationen zum Definieren benutzerdefinierter Eigenschaften finden Sie unter [Definieren neuer MAPI-Eigenschaften.](defining-new-mapi-properties.md)
  
> [!NOTE]
> Formularserver mit einem Nachrichtentext verwenden häufig die **Eigenschaft PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), um sie zu speichern. Wenn ihr Formularserver **PR_RTF_COMPRESSED** verwendet, sollte außerdem sichergestellt werden, dass die **eigenschaft PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) eine textgeschützte Version des Nachrichtentexts enthält, falls die resultierende Nachricht von einem Client gelesen wird, der RTF-Nachrichtentext (Rich Text Format) nicht unterstützt. 
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

