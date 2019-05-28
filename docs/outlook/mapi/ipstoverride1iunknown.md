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
  
Ermöglicht einem PST-Speicheranbieter (Personal Folders File) das außer Kraft setzen der PSTDisableGrow-Richtlinie.
  
|||
|:-----|:-----|
|Erbt von:  <br/> |IUnknown  <br/> |
|Implementiert von:  <br/> |PST-Speicheranbieter  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Ruft die Liste der Registrierungen für die persönliche Ordner-Datei (PST) ab.  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Registriert persönliche Ordner-Dateien für die automatische Entriegelung und verhindert weitere Aufrufe an HrTrustedPSTOverrideHandlerCallback.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Entsperrt eine persönliche Ordner-Datei für Wachstum.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die Schnittstellenbezeichner für den PST-Außerkraftsetzungs Handler sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben, in diesem Fall werden Sie Sie im Thema [MAPI-Konstanten](mapi-constants.md) finden, und Sie können Sie kopieren und Ihrem Code hinzufügen. Verwenden Sie das DEFINE_GUID-Makro, das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef. h definiert ist, um GUID-symbolische Namen (Globally Unique Identifier) mit ihren Werten zu verknüpfen. 
  
Weitere Informationen finden Sie unter [How to implement a PST override Handler to Bypass the PSTDisableGrow Policy in Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Siehe auch



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

