---
title: Unterstützung von RTF-Text für Store-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dc1d8a5e237b7b34f3a57e9789e03e2f16237764
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414214"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>Unterstützung von RTF-Text für Store-Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Clientanwendungen ermöglichen Benutzern die Verwendung von Rich Text Format (RTF)-Text in ihren Nachrichten. Wenn Ihr Nachrichtenspeicheranbieter #A0 in Nachrichten unterstützen muss, muss er die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) -Eigenschaft zusätzlich zur **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft behandeln. Dies bedeutet in erster Linie, beide Eigenschaften zu speichern und sicherzustellen, dass **PR_BODY** eine Nur-Text-Version des Texts **in** PR_RTF_COMPRESSED. Die [RTFSync-Funktion](rtfsync.md) ist zu diesem Zweck nützlich. 
  
Es gibt zwei Kennzeichen, die in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Nachrichtenspeicherobjekts festgelegt werden können, die Clients mitteilen, was sie vom Nachrichtenspeicheranbieter im Hinblick auf die **Eigenschaften PR_BODY** und **PR_RTF_COMPRESSED** für Nachrichten im Nachrichtenspeicher erwarten können. Das STORE_RTF_OK gibt an, dass der Speicher den Wert der **PR_BODY-Eigenschaft** aus der **PR_RTF_COMPRESSED-Eigenschaft** dynamisch generieren kann, wodurch Clients nicht explizit synchronisiert werden müssen. Das STORE_UNCOMPRESSED_RTF gibt an, dass der Nachrichtenspeicheranbieter nicht komprimierte Daten **in** PR_RTF_COMPRESSED.
  
Nachrichtenspeicheranbieter, die #A0 nicht unterstützen, müssen die **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))-Eigenschaft löschen, wenn sich die **PR_BODY-Eigenschaft** ändert, um ordnungsgemäß mit Clientanwendungen zu arbeiten, die #A1 unterstützen. 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

