---
title: IMAPIContainer IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5a76b5cb08e098235dda03df81becf9b15c6ee69
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610657"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet allgemeine Vorgänge für Containerobjekte wie Adressbücher, Verteilerlisten und Ordner. Die [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)und [IDistList : IMAPIContainer-Schnittstellen](idistlistimapicontainer.md) werden von **IMAPIContainer** abgeleitet.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Ordner-, Adressbuchcontainer- und Verteilerlistenobjekte  <br/> |
|Implementiert von:  <br/> |Nachrichtenspeicher, Adressbuch und Remote-Transportanbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIContainer  <br/> |
|Zeigertyp:  <br/> |LPMAPICONTAINER  <br/> |
|Transaktionsmodell:  <br/> |Abstrakte Klasse, nie implementiert  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[GetContentsTable](imapicontainer-getcontentstable.md) <br/> |Gibt einen Zeiger auf das Inhaltsverzeichnis des Containers zurück.  <br/> |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |Gibt einen Zeiger auf die Hierarchietabelle des Containers zurück.  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Öffnet ein Objekt im Container und gibt einen Schnittstellenzeiger für den weiteren Zugriff zurück.  <br/> |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |Legt Suchkriterien für den Container fest.  <br/> |
|[GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |Ruft die Suchkriterien für den Container ab.  <br/> |
   
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

