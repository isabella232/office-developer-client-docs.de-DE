---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315498"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht einem Anbieter für den Informationsspeicher für persönliche Ordner (PST) das Außerkraft setzen der PSTDisableGrow-Richtlinie.
  
|||
|:-----|:-----|
|Erbt von:  <br/> |IUnknown  <br/> |
|Implementiert von:  <br/> |Anbieter für den PST-Speicher  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Ruft die Liste der Registrierungen für die Datei Persönliche Ordner (PST) ab.  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Registriert Persönliche Ordnerdateien für die automatische Entsperrung, um weitere Aufrufe von HrTrustedPSTOverrideHandlerCallback zu vermeiden.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Entsperrt eine Datei mit persönlichen Ordnern für das Wachstum.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die Pst Override Handler Interface Identifiers sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall finden Sie sie im Thema [MAPI-Konstanten](mapi-constants.md) und können sie kopieren und ihrem Code hinzufügen. Verwenden Sie das DEFINE_GUID, das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef.h definiert ist, um ihren Werten symbolische Namen (Globally Unique Identifier, GUID) zuzuordnen. 
  
Weitere Informationen finden Sie unter Implementieren eines PST-Außerkraftsetzungshandlers zum Umgehen der [PSTDisableGrow-Richtlinie in Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Siehe auch



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

