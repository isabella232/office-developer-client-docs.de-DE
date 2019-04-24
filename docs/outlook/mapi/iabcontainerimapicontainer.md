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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348958"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf Adressbuchcontainer. MAPI-und Clientanwendungen rufen die Methoden von **IABContainer** auf, um die Namensauflösung auszuführen und Empfänger zu erstellen, zu kopieren und zu löschen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Adressbuchcontainer-Objekte  <br/> |
|Implementiert von:  <br/> |Adressbuchanbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI-und Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IABContainer  <br/> |
|Zeigertyp:  <br/> |LPABCONT  <br/> |
|Transaktionsmodell:  <br/> |Durchgeführt  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[CreateEntry](iabcontainer-createentry.md) <br/> |Erstellt einen neuen Eintrag, bei dem es sich um einen Messagingbenutzer, eine Verteilerliste oder einen anderen Container handeln kann.  <br/> |
|[CopyEntries](iabcontainer-copyentries.md) <br/> |Kopiert einen oder mehrere Einträge, in der Regel Messagingbenutzer oder Verteilerlisten.  <br/> |
|[DeleteEntries](iabcontainer-deleteentries.md) <br/> |Entfernt einen oder mehrere Einträge, in der Regel Messagingbenutzer, Verteilerlisten oder andere Container.  <br/> |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |Führt die Namensauflösung für einen oder mehrere Empfänger Einträge aus.  <br/> |
   
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_FLAGS** ([Pidtagcontainerflags (](pidtagcontainerflags-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
|**Optionale Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_DEF_CREATE_DL** ([Pidtagdefcreatedl (](pidtagdefcreatedl-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_DEF_CREATE_MAILUSER** ([Pidtagdefcreatemailuser (](pidtagdefcreatemailuser-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die **IABContainer** -Schnittstelle erbt indirekt von der [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) -Schnittstelle über die [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) und [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstellen. Adressbuchanbieter implementieren die **IABContainer** -Schnittstelle. 
  
Eine beliebige Anzahl von Messaging-Benutzerobjekten, Verteilerlisten und anderen Adressbuch Containern kann in einem Adressbuchcontainer vorhanden sein. Wie bei jedem Container können Clients oder Dienstanbieter einen Adressbuchcontainer verwenden, um einen seiner Einträge zu öffnen oder um eine Hierarchietabelle oder eine Inhaltstabelle abzurufen. Adressbuchcontainer bieten außerdem eine Namensauflösung und je nach Anbieter die Möglichkeit, Einträge hinzuzufügen, zu entfernen oder zu ändern.
  
MAPI definiert einen speziellen Adressbuchcontainer, der als persönliches Adressbuch (PAB) bezeichnet wird und Einträge aus anderen Containern enthält. Ein PAB kann immer geändert werden. Benutzer füllen Ihr PAB in der Regel mit Einträgen, die die Empfänger angeben, mit denen Sie am häufigsten kommunizieren. Ein PAB kann auch einmalige Adressen und neue Empfänger enthalten, die noch nicht Bestandteileines Adressbuch Containers sind.
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Schnittstellen](mapi-interfaces.md)

