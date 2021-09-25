---
title: IPropData IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a590f5188d33d7fac0600f341d2c0fdef755b8e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579740"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet die Möglichkeit, den Zugriff für die Eigenschaften eines Objekts abzurufen und zu ändern. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Property Data-Objekt  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter und Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIPropData  <br/> |
|Zeigertyp:  <br/> |LPPROPDATA  <br/> |
|Transaktionsmodell:  <br/> |Nicht übersetzt  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |Legt die Zugriffsebene f�r das Objekt fest.  <br/> |
|[HrSetPropAccess](ipropdata-hrsetpropaccess.md) <br/> |Legt die Zugriffsebene und den Status für eine oder mehrere Eigenschaften des Objekts fest.  <br/> |
|[HrGetPropAccess](ipropdata-hrgetpropaccess.md) <br/> |Ruft die Zugriffsebene und den Status f�r eine oder mehrere der Eigenschaften des Objekts an.  <br/> |
|[HrAddObjProps](ipropdata-hraddobjprops.md) <br/> |Fügt dem Objekt eine oder mehrere Eigenschaften vom Typ PT_OBJECT hinzu.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die **IPropData::IMAPIProp-Schnittstelle** wird von der MAPI implementiert und hauptsächlich von Dienstanbietern verwendet, die durch Aufrufen der [CreateIProp-Funktion](createiprop.md) auf diese Implementierung zugreifen. 
  
Weitere Informationen zu Zugriffsebenen für Objekte und Eigenschaften finden Sie unter ["Berechtigungen für Objekte und Eigenschaften".](permissions-for-mapi-objects-and-properties.md)
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

