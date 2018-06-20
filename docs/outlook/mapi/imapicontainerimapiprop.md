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
ms.openlocfilehash: e24f5ebd73a4652876282099f1460762c150b94d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792078"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer: IMAPIProp

  
  
**Betrifft**: Outlook 
  
Allgemeine Vorgänge auf Containerobjekten wie Adressbücher, Verteilerlisten und Ordner verwaltet. Die [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md), und [IDistList: IMAPIContainer](idistlistimapicontainer.md) Schnittstellen **IMAPIContainer**abgeleitet sind.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Ordner, Adressbuchcontainer und Verteilung List-Objekten  <br/> |
|Implementiert von:  <br/> |Nachrichtenspeicher, Adressbuch und remote-Transport-Anbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIContainer  <br/> |
|Zeigertyp:  <br/> |LPMAPICONTAINER  <br/> |
|Transaktionsmodell:  <br/> |Abstrakte Basisklasse, die nie implementiert  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetContentsTable](imapicontainer-getcontentstable.md) <br/> |Gibt einen Zeiger auf den Container Inhaltstabelle.  <br/> |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |Gibt einen Zeiger auf den Container Hierarchietabelle.  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Öffnet ein Objekt im Container einen Schnittstellenzeiger für den weiteren Zugriff zurückgibt.  <br/> |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |Stellt die Suchkriterien für den Container her.  <br/> |
|[GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |Ruft die Suchkriterien für den Container an.  <br/> |
   
|**Erforderliche Eigenschaften**|**Zugriff**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

