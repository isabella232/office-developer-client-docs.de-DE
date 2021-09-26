---
title: Unterstützung von RTF-Text für Nachrichten Store Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 699d736e61a7bee2bb775a3563ce73327b97b955
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629480"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>Unterstützung von RTF-Text für Nachrichten Store Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Clientanwendungen ermöglichen Es Benutzern, RTF-Text (Rich Text Format) in ihren Nachrichten zu verwenden. Wenn Ihr Nachrichtenspeicheranbieter RTF-Text in Nachrichten unterstützen muss, muss er die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) -Eigenschaft zusätzlich zur **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft behandeln. In erster Linie bedeutet dies, beide Eigenschaften zu speichern und sicherzustellen, dass **PR_BODY** eine Nur-Text-Version des Texts in **PR_RTF_COMPRESSED** enthält. Die [RTFSync-Funktion](rtfsync.md) ist für diesen Zweck nützlich. 
  
Es gibt zwei Flags, die in der **Eigenschaft PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) des Nachrichtenspeicherobjekts festgelegt werden können, die Clients mitteilen, was sie vom Nachrichtenspeicheranbieter in Bezug auf die **PR_BODY** und **PR_RTF_COMPRESSED** Eigenschaften für Nachrichten im Nachrichtenspeicher erwarten können. Das flag STORE_RTF_OK gibt an, dass der Speicher den Wert der **PR_BODY-Eigenschaft** dynamisch aus der **PR_RTF_COMPRESSED-Eigenschaft** generieren kann, wodurch Clients die Last der expliziten Synchronisierung vermeiden können. Das flag STORE_UNCOMPRESSED_RTF gibt an, dass der Nachrichtenspeicheranbieter nicht komprimierte Daten in **PR_RTF_COMPRESSED** unterstützen kann.
  
Nachrichtenspeicheranbieter, die RTF-Text nicht unterstützen, müssen die **eigenschaft PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) löschen, wenn sich die **PR_BODY-Eigenschaft** ändert, um ordnungsgemäß mit Clientanwendungen zusammenarbeiten zu können, die RTF-Text unterstützen. 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

