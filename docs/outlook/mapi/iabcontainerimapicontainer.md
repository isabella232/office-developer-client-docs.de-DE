---
title: IABContainer IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer
api_type:
- COM
ms.assetid: 1f5ce6e0-b79a-4da2-b014-8c00cd72912e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348958"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf Adressbuchcontainer. MAPI- und Clientanwendungen rufen die Methoden von **IABContainer** auf, um Namensauflösungen durchzuführen und Empfänger zu erstellen, zu kopieren und zu löschen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Adressbuchcontainerobjekte  <br/> |
|Implementiert von:  <br/> |Adressbuchanbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI- und Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IABContainer  <br/> |
|Zeigertyp:  <br/> |LPABCONT  <br/> |
|Transaktionsmodell:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[CreateEntry](iabcontainer-createentry.md) <br/> |Erstellt einen neuen Eintrag, der ein Messagingbenutzer, eine Verteilerliste oder ein anderer Container sein kann.  <br/> |
|[CopyEntries](iabcontainer-copyentries.md) <br/> |Kopiert einen oder mehrere Einträge, in der Regel Messagingbenutzer oder Verteilerlisten.  <br/> |
|[DeleteEntries](iabcontainer-deleteentries.md) <br/> |Entfernt einen oder mehrere Einträge, in der Regel Messagingbenutzer, Verteilerlisten oder andere Container.  <br/> |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |Führt die Namensauflösung für einen oder mehrere Empfängereinträge aus.  <br/> |
   
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
|**Optionale Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Hinweise

Die **IABContainer-Schnittstelle** erbt indirekt von der [IUnknown-Schnittstelle](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) über die [SCHNITTSTELLEN IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) und [IMAPIProp : IUnknown.](imapipropiunknown.md) Adressbuchanbieter implementieren die **IABContainer-Schnittstelle.** 
  
Eine beliebige Anzahl von Messagingbenutzerobjekten, Verteilerlisten und anderen Adressbuchcontainern kann in einem Adressbuchcontainer vorhanden sein. Wie bei jedem Container können Clients oder Dienstanbieter einen Adressbuchcontainer verwenden, um einen seiner Einträge zu öffnen oder eine Hierarchietabelle oder Inhaltstabelle abzurufen. Adressbuchcontainer bieten auch die Namensauflösung und je nach Anbieter die Möglichkeit, Einträge hinzuzufügen, zu entfernen oder zu ändern.
  
MAPI definiert einen speziellen Adressbuchcontainer namens Persönliches Adressbuch (PAB), der Einträge enthält, die aus anderen Containern kopiert wurden. Ein PAB ist immer veränderbar. Benutzer füllen ihr PAB in der Regel mit Einträgen auf, mit denen die Empfänger bezeichnet werden, mit denen sie am häufigsten kommunizieren. Ein PAB kann auch einmal adressen und neue Empfänger enthalten, die noch nicht Teil eines Adressbuchcontainers sind.
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Schnittstellen](mapi-interfaces.md)

