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
ms.openlocfilehash: 38094895fed03884b138b02d4aa1ed87bcc6ea9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575700"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Allgemeine Vorgänge auf Containerobjekten wie Adressbücher, Verteilerlisten und Ordner verwaltet. Die [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md), und [IDistList: IMAPIContainer](idistlistimapicontainer.md) Schnittstellen **IMAPIContainer**abgeleitet sind.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verfügbar gemacht von:  <br/> |Ordner, Adressbuchcontainer und Verteilung List-Objekten  <br/> |
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
   
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

