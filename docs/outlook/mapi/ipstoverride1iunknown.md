---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0e518fc9ea0e7f4b4b4576b45a06ec7c0fe2e303
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556308"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht einem PST-Speicheranbieter (Personal Folders File), die PSTDisableGrow-Richtlinie außer Kraft zu setzen.
  
|||
|:-----|:-----|
|Erbt von:  <br/> |IUnknown  <br/> |
|Implementiert von:  <br/> |ANBIETER DES PST-Speichers  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Ruft die Liste der Registrierungen für die Datei "Persönliche Ordner" (PST) ab.  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Registriert persönliche Ordnerdateien für die automatische Entsperrung, um weitere Aufrufe von HrTrustedPSTOverrideHandlerCallback zu vermeiden.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Entsperrt eine persönliche Ordnerdatei für das Wachstum.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die PST Override Handler Interface Identifiers sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall finden Sie sie im Thema [zu MAPI-Konstanten](mapi-constants.md) und können sie kopieren und ihrem Code hinzufügen. Verwenden Sie das DEFINE_GUID Makro, das in der Guiddef.h-Headerdatei des Microsoft Windows Software Development Kit (SDK) definiert ist, um ihren Werten symbolische GUID-Namen (Globally Unique Identifier) zuzuordnen. 
  
Weitere Informationen finden Sie unter [Implementieren eines PST-Überschreibungshandlers zum Umgehen der PSTDisableGrow-Richtlinie in Outlook 2007.](https://support.microsoft.com/kb/956070)
  
## <a name="see-also"></a>Siehe auch



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

