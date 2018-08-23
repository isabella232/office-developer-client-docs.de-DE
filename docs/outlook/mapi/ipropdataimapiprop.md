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
ms.openlocfilehash: c320b2c42b9a14c6dc428fc3df59991528cdbe36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592570"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bietet die Möglichkeit zum Abrufen und ändern Sie den Zugriff für die Eigenschaften eines Objekts. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Verfügbar gemacht von:  <br/> |Property-Daten-Objekt  <br/> |
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Die **IPropData::IMAPIProp** -Schnittstelle wird von MAPI implementierte und in erster Linie vom Dienstanbieter, die dieser Implementierung zugreifen, indem die [CreateIProp](createiprop.md) -Funktion verwendet. 
  
Weitere Informationen zu Zugriffsebenen-Objekten und Eigenschaften finden Sie unter [Berechtigungen für Objekte und Eigenschaften](permissions-for-mapi-objects-and-properties.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

