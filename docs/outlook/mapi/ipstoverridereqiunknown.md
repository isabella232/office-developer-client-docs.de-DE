---
title: IPSTOVERRIDEREQ IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1f851d098819b583ab5a6e65b306e97ba01885e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587839"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Greift auf Ressourcen eines PST-Speicheranbieters (Personal Folders File) zu.
  
|||
|:-----|:-----|
|Erbt von:  <br/> |IUnknown  <br/> |
|Implementiert von:  <br/> |ANBIETER DES PST-Speichers  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Initiiert die Entsperrungsprozedur für eine persönliche Ordnerdatei (PST).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die PST Override Handler Interface Identifiers sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall finden Sie sie im Thema [zu MAPI-Konstanten](mapi-constants.md) und können sie kopieren und ihrem Code hinzufügen. Verwenden Sie das DEFINE_GUID Makro, das in der Guiddef.h-Headerdatei des Microsoft Windows Software Development Kit (SDK) definiert ist, um symbolischen GUID-Namen (Globally Unique Identifier) ihren Werten zuzuordnen. 
  
Weitere Informationen finden Sie unter [Implementieren eines PST-Überschreibungshandlers zum Umgehen der PSTDisableGrow-Richtlinie in Outlook 2007.](https://support.microsoft.com/kb/956070)
  
## <a name="see-also"></a>Siehe auch



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

