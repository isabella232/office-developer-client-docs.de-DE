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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7f3f6ae2b9849710bf44d3635fc7bb9a62016f48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356980"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Greift auf Ressourcen eines PST-Speicheranbieters (Personal Folders File) zu.
  
|||
|:-----|:-----|
|Erbt von:  <br/> |IUnknown  <br/> |
|Implementiert von:  <br/> |PST-Speicheranbieter  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Initiiert die entsperrungs Prozedur für eine persönliche Ordner-Datei (PST).  <br/> |
   
## <a name="remarks"></a>Hinweise

Die Schnittstellenbezeichner für den PST-Außerkraftsetzungs Handler sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben, in diesem Fall werden Sie Sie im Thema [MAPI-Konstanten](mapi-constants.md) finden, und Sie können Sie kopieren und Ihrem Code hinzufügen. Verwenden Sie das DEFINE_GUID-Makro, das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef. h definiert ist, um GUID-symbolische Namen (Globally Unique Identifier) mit ihren Werten zu verknüpfen. 
  
Weitere Informationen finden Sie unter [How to implement a PST override Handler to Bypass the PSTDisableGrow Policy in Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Siehe auch



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

