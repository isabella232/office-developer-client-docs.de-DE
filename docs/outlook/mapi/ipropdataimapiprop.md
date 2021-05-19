---
title: IPropData IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aed9120ac264a6c47c9d02502093e56d3268d08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435145"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht das Abrufen und Ändern des Zugriffs für die Eigenschaften eines Objekts. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Eigenschaftsdatenobjekt  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter und Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIPropData  <br/> |
|Zeigertyp:  <br/> |LPPROPDATA  <br/> |
|Transaktionsmodell:  <br/> |Nichttransaktioniert  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |Legt die Zugriffsebene f�r das Objekt fest.  <br/> |
|[HrSetPropAccess](ipropdata-hrsetpropaccess.md) <br/> |Legt die Zugriffsebene und den Status für eine oder mehrere Eigenschaften des Objekts fest.  <br/> |
|[HrGetPropAccess](ipropdata-hrgetpropaccess.md) <br/> |Ruft die Zugriffsebene und den Status f�r eine oder mehrere der Eigenschaften des Objekts an.  <br/> |
|[HrAddObjProps](ipropdata-hraddobjprops.md) <br/> |Fügt eine oder mehrere Eigenschaften vom Typ PT_OBJECT objekt hinzu.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die **IPropData::IMAPIProp-Schnittstelle** wird von MAPI implementiert und hauptsächlich von Dienstanbietern verwendet, die auf diese Implementierung zugreifen, indem sie die [CreateIProp-Funktion](createiprop.md) aufrufen. 
  
Weitere Informationen zu Zugriffsebenen für Objekte und Eigenschaften finden Sie unter [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

