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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8be3b1857d539f81e42d2ac3e5813afa73513a16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286720"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet Vorgänge auf hoher Ebene für Containerobjekte wie Adressbücher, Verteilerlisten und Ordner. Die [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)und [IDistList: IMAPIContainer](idistlistimapicontainer.md) -Schnittstellen werden von **IMAPIContainer**abgeleitet.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Ordner-, Adressbuchcontainer-und Verteilerlistenobjekte  <br/> |
|Implementiert von:  <br/> |Nachrichtenspeicher, Adressbuch und Remote Transportanbieter  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIContainer  <br/> |
|Zeigertyp:  <br/> |LPMAPICONTAINER  <br/> |
|Transaktionsmodell:  <br/> |Abstrakte Klasse, nie implementiert  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetContentable](imapicontainer-getcontentstable.md) <br/> |Gibt einen Zeiger auf die Inhaltstabelle des Containers zurück.  <br/> |
|[GetHierarchy-Struktur](imapicontainer-gethierarchytable.md) <br/> |Gibt einen Zeiger auf die Hierarchietabelle des Containers zurück.  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Öffnet ein Objekt im Container und gibt einen Schnittstellenzeiger für den weiteren Zugriff zurück.  <br/> |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |Legt Suchkriterien für den Container fest.  <br/> |
|[GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |Ruft die Suchkriterien für den Container ab.  <br/> |
   
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_CONTAINER_CONTENTS** ([Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_CONTAINER_FLAGS** ([Pidtagcontainerflags (](pidtagcontainerflags-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

