---
title: IMAPIContainer IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8be3b1857d539f81e42d2ac3e5813afa73513a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406122"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet vorgänge auf hoher Ebene für Containerobjekte wie Adressbücher, Verteilerlisten und Ordner. The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Ordner-, Adressbuchcontainer- und Verteilerlistenobjekte  <br/> |
|Implementiert von:  <br/> |Nachrichtenspeicher, Adressbuch und Remotetransportanbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIContainer  <br/> |
|Zeigertyp:  <br/> |LPMAPICONTAINER  <br/> |
|Transaktionsmodell:  <br/> |Abstrakte Klasse, nie implementiert  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetContentsTable](imapicontainer-getcontentstable.md) <br/> |Gibt einen Zeiger auf die Inhaltstabelle des Containers zurück.  <br/> |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |Gibt einen Zeiger auf die Hierarchietabelle des Containers zurück.  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Öffnet ein Objekt im Container und gibt einen Schnittstellenzeiger für weiteren Zugriff zurück.  <br/> |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |Legt Suchkriterien für den Container fest.  <br/> |
|[GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |Ruft die Suchkriterien für den Container ab.  <br/> |
   
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

