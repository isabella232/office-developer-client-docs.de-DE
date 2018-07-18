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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d6a53d112e4c12cd9092ac627e99cf3c13d901f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792770"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**Betrifft**: Outlook 
  
Bietet die Möglichkeit zum Abrufen und ändern Sie den Zugriff für die Eigenschaften eines Objekts. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Property-Daten-Objekt  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter und -Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIPropData  <br/> |
|Zeigertyp:  <br/> |LPPROPDATA  <br/> |
|Transaktionsmodell:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |Legt die Zugriffsebene f�r das Objekt fest.  <br/> |
|[HrSetPropAccess](ipropdata-hrsetpropaccess.md) <br/> |Die Zugriffsebene und den Status für eine oder mehrere der Eigenschaften des Objekts festgelegt.  <br/> |
|[HrGetPropAccess](ipropdata-hrgetpropaccess.md) <br/> |Ruft die Zugriffsebene und den Status f�r eine oder mehrere der Eigenschaften des Objekts an.  <br/> |
|[HrAddObjProps](ipropdata-hraddobjprops.md) <br/> |Fügt eine oder mehrere Eigenschaften vom Typ PT_OBJECT auf das Objekt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die **IPropData::IMAPIProp** -Schnittstelle wird von MAPI implementierte und in erster Linie vom Dienstanbieter, die dieser Implementierung zugreifen, indem die [CreateIProp](createiprop.md) -Funktion verwendet. 
  
Weitere Informationen zu Zugriffsebenen-Objekten und Eigenschaften finden Sie unter [Berechtigungen für Objekte und Eigenschaften](permissions-for-mapi-objects-and-properties.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

