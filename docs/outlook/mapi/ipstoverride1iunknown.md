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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: db2853080b1fc2ff3a346dcfb8d112237b7f3459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792813"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1: IUnknown

  
  
**Betrifft**: Outlook 
  
Ermöglicht einen Anbieter für Persönliche Ordner-Datei (PST) anmelden die PSTDisableGrow Richtlinie außer Kraft gesetzt.
  
|||
|:-----|:-----|
|Erbt:  <br/> |IUnknown  <br/> |
|Implementiert von:  <br/> |PST-Anbieter  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Ruft die Liste von Einträgen für den persönlichen Ordner (PST) Datei ab.  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Registriert Persönliche Ordner-Dateien für die automatische Entsperren Weitere Anrufe an HrTrustedPSTOverrideHandlerCallback zu vermeiden.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Hebt die Sperre für das Wachstum der Persönliche Ordner-Datei.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die PST-Datei überschreiben Handler Schnittstellenbezeichner möglicherweise nicht in der herunterladbaren Headerdatei definiert werden derzeit, in diesem Fall müssen Sie finden sie im Thema [MAPI-Konstanten](mapi-constants.md) und können kopieren und fügen sie dem Code hinzu. Verwenden Sie das DEFINE_GUID-Makro in der Microsoft Windows Software Development Kit (SDK)-Header-Datei guiddef.h definiert, deren Werte symbolische Namen global eindeutigen Bezeichner (GUID) zugeordnet. 
  
Weitere Informationen finden Sie unter [ein PST Außerkraftsetzung Handler für die Umgehung die PSTDisableGrow Richtlinie in Outlook 2007 implementiert wird](http://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Siehe auch



[IPSTOVERRIDEREQ: IUnknown](ipstoverridereqiunknown.md)

