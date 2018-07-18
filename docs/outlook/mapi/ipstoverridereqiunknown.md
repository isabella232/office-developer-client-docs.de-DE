---
title: IPSTOVERRIDEREQ IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6ee4524d08e334df858c2f035f1b21bd2b0a1c8b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792806"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**Betrifft**: Outlook 
  
Greift auf Ressourcen in einen Anbieter für Persönliche Ordner-Datei (PST) anmelden.
  
|||
|:-----|:-----|
|Erbt:  <br/> |IUnknown  <br/> |
|Implementiert von:  <br/> |PST-Anbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Initiiert das Aufheben der Sperre Verfahren für den persönlichen Ordner (PST).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die PST-Datei überschreiben Handler Schnittstellenbezeichner möglicherweise nicht in der herunterladbaren Headerdatei definiert werden derzeit, in diesem Fall müssen Sie finden sie im Thema [MAPI-Konstanten](mapi-constants.md) und können kopieren und fügen sie dem Code hinzu. Verwenden Sie das DEFINE_GUID-Makro in der Microsoft Windows Software Development Kit (SDK)-Header-Datei guiddef.h definiert, deren Werte symbolische Namen global eindeutigen Bezeichner (GUID) zugeordnet. 
  
Weitere Informationen finden Sie unter [ein PST Außerkraftsetzung Handler für die Umgehung die PSTDisableGrow Richtlinie in Outlook 2007 implementiert wird](http://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Siehe auch



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

