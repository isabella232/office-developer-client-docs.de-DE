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
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Initiiert das Entriegelungs Verfahren für eine persönliche Ordner-Datei (PST).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die PST-überSchreibungs-Handler-Schnittstellenbezeichner sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben, in diesem Fall finden Sie Sie im Thema [MAPI-Konstanten](mapi-constants.md) und können Sie zu Ihrem Code kopieren und hinzufügen. Verwenden Sie das DEFINE_GUID-Makro, das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef. h definiert ist, um symbolische GUIDs (Globally Unique Identifier) mit ihren Werten zu verknüpfen. 
  
Weitere Informationen finden Sie unter [Implementieren eines PST-Überschreibungs Handlers, um die PSTDisableGrow-Richtlinie in Outlook 2007 zu umgehen](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Siehe auch



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

