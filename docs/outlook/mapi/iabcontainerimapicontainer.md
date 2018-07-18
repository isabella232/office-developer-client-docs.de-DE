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
ms.openlocfilehash: 0eb6d62b64595474957415e94275d0ac52cc2b6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791954"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**Betrifft**: Outlook 
  
Bietet Zugriff auf Address Book Container. MAPI-und Clientanwendungen rufen Sie die Methoden des **IABContainer** namensauflösung ausführen, und kopieren Sie Sie zum Erstellen und Löschen von Empfängern. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Address Book Container-Objekte  <br/> |
|Implementiert von:  <br/> |Von adressbuchanbietern implementierte  <br/> |
|Aufgerufen von:  <br/> |MAPI-und Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IABContainer  <br/> |
|Zeigertyp:  <br/> |LPABCONT  <br/> |
|Transaktionsmodell:  <br/> |Durchgeführt  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[CreateEntry](iabcontainer-createentry.md) <br/> |Erstellt einen neuen Eintrag, der ein messaging-Benutzer, eine Verteilerliste oder einen anderen Container sein kann.  <br/> |
|[CopyEntries](iabcontainer-copyentries.md) <br/> |Kopiert eine oder mehrere Einträge, in der Regel messaging Benutzer oder Verteilerlisten.  <br/> |
|[DeleteEntries](iabcontainer-deleteentries.md) <br/> |Entfernt einen oder mehrere Einträge in der Regel messaging Benutzern, Verteilerlisten oder andere Container.  <br/> |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |Führt die Auflösung für einen oder mehrere Empfänger Einträge.  <br/> |
   
|**Erforderliche Eigenschaften**|**Zugriff**|
|:-----|:-----|
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
   
|**Optionale Eigenschaften**|**Zugriff**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die **IABContainer** -Schnittstelle erbt indirekt von [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) -Schnittstelle, über die [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) und [IMAPIProp: IUnknown](imapipropiunknown.md) Schnittstellen. Von adressbuchanbietern implementierte implementieren die **IABContainer** -Schnittstelle. 
  
Eine beliebige Anzahl von messaging User-Objekte, Verteilerlisten und andere Address Book-Container kann in einer Adressbuchcontainer vorhanden sein. Wie bei einem beliebigen Container können Clients oder Dienstanbieter ein Adressbuchcontainer öffnen Sie eine der zugehörigen Einträge oder einer Hierarchietabelle oder Inhaltstabelle abrufen. Adressbuch Container auch eine namensauflösung und, abhängig von des Anbieters die Möglichkeit zum Hinzufügen, entfernen oder Ändern von Einträgen.
  
MAPI definiert eine spezielle Adressbuchcontainer bezeichnet das persönliche Adressbuch (PAB), das von anderen Containern kopierten Einträge enthält. Ein PAB kann jederzeit geändert werden. Benutzer füllen ihre PAB in der Regel mit Einträgen Festlegen der Empfänger an, mit denen sie am häufigsten kommunizieren. Ein PAB kann auch einmal-Adressen und neue Empfänger noch nicht Teil der alle Adressbuchcontainer halten.
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Schnittstellen](mapi-interfaces.md)

