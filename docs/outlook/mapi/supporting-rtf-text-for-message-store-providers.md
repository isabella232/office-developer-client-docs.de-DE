---
title: Unterstützen von RTF-Text für Nachrichtenspeicher Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dc1d8a5e237b7b34f3a57e9789e03e2f16237764
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349616"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>Unterstützen von RTF-Text für Nachrichtenspeicher Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Clientanwendungen ermöglichen es Benutzern, RTF-Text (Rich Text Format) in ihren Nachrichten zu verwenden. Wenn der Nachrichtenspeicher Anbieter RTF-Text in Nachrichten unterstützen muss, muss er zusätzlich zur **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft behandeln. Dies ist in erster Linie das Speichern beider Eigenschaften und das sicherstellen, dass **PR_BODY** eine nur-Text-Version des Texts in **PR_RTF_COMPRESSED**enthält. Die [RTFSync](rtfsync.md) -Funktion ist für diesen Zweck nützlich. 
  
Es gibt zwei Flags, die in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Nachrichtenspeicher Objekts festgelegt werden können, die den Clients mitteilen, was Sie vom Nachrichtenspeicher Anbieter im Hinblick auf **PR_BODY** und PR_ erwarten können. ** RTF_COMPRESSED** -Eigenschaften für Nachrichten im Nachrichtenspeicher. Das STORE_RTF_OK-Flag gibt an, dass der Speicher den Wert der **PR_BODY** -Eigenschaft aus der **PR_RTF_COMPRESSED** -Eigenschaft dynamisch generieren kann, wodurch Clients von der Last der expliziten Synchronisierung entlastet werden. Das STORE_UNCOMPRESSED_RTF-Flag gibt an, dass der Nachrichtenspeicher Anbieter nicht komprimierte Daten in **PR_RTF_COMPRESSED**unterstützenkann.
  
Nachrichtenspeicher Anbieter, die keinen RTF-Text unterstützen, müssen die **PR_RTF_IN_SYNC** ([pidtagrtfinsync (](pidtagrtfinsync-canonical-property.md))-Eigenschaft löschen, wenn sich die **PR_BODY** -Eigenschaft ändert, um ordnungsgemäß mit CLIENTanwendungen zu interagieren, die RTF-Text unterstützen. . 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

