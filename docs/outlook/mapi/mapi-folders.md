---
title: MAPI-Ordner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8fac3c92-d2f5-479e-a368-ca82bddd8e30
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6c00dce9ec489ca2b886f3e51551ba57e9eeea33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421844"
---
# <a name="mapi-folders"></a>MAPI-Ordner

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ordner sind MAPI-Objekten, die als Basiseinheit Organisation f�r Nachrichten zu bedienen. Hierarchisch angeordnet sind, k�nnen Ordner Nachrichten und andere Ordner enthalten. Ordner erleichtern das Suchen von und Arbeiten mit Nachrichten.
  
Ordner implementieren Sie die [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle, die indirekt von der **IUnknown** -Schnittstelle, durch die [IMAPIContainer](imapicontainerimapiprop.md) und [IMAPIProp](imapipropiunknown.md) Schnittstellen erbt. Clients verwenden **IMAPIFolder** erstellen, kopieren und L�schen von Nachrichten und Ordnern, abrufen und Festlegen des Nachrichtenstatus, und so festlegen oder Aufheben der Kennzeichnung Lesen einer Nachricht. Obwohl Nachricht-Anbieter zur Unterst�tzung aller Methoden in **IMAPIFolder** erforderlich sind, stellen Sie einige Methoden Ma� an Komplexit�t, die Nachricht Anbieter vermeiden m�chten m�glicherweise vor. MAPI sparen-Anbieter Nachricht einige Arbeit einige komplexere Ordner Funktionen in der [IMAPISupport](imapisupportiunknown.md) -Schnittstelle implementieren. Anstatt einen eigenen Kopie-Methoden implementieren, beispielsweise k�nnen Nachricht Anbieter rufen die Methoden Kopie im Support-Objekt und die gleichen Ergebnisse erhalten m�chten. 
  
Es gibt drei Arten von Ordnern:
  
- Stammordner.
    
- Generische Ordner.
    
- Suchordner
    
Jeder Nachrichtenspeicher hat mindestens eine Stammordner. Stammordner wird oben in der Hierarchie und Nachrichten und andere Ordner enth�lt. Stammordner k�nnen nicht verschoben, kopiert, umbenannt oder gel�scht werden. Es gibt nur eine Stammordner f�r jeden Nachrichtenspeicher.
  
Die meisten anderen Ordner sind generische Ordner. Generische Ordner enthalten wie Stammordner Nachrichten und anderen Ordner. Im Gegensatz zum Stammordner k�nnen sie verschoben, kopiert, umbenannt und gel�scht werden. Generische Ordner k�nnen in den Stammordner oder andere generische Ordner erstellt werden. Wenn ein Client einen generischen Ordner in einem anderen Ordner erstellt, wird der neue Ordner einen Unterordner oder untergeordneten Ordner aufgerufen. Der Ordner, in dem Sie der neue Ordner befindet, wird als des �bergeordneten Ordners des neuen Ordners bezeichnet. Generische Ordner mit dem gleichen �bergeordneten Ordner werden als gleichgeordnete Ordner bezeichnet. Gleichgeordneten Knoten und nicht gleichgeordnete Ordner m�glicherweise oder m�glicherweise nicht eindeutige Namen haben, je nach der Nachricht Speicheranbieter. Nachricht-Anbieter, die gleichgeordnete Ordner haben eindeutige Namen den Fehlerwert MAPI_E_COLLISION zur�ck, wenn ein Client versucht, erstellen Sie zwei Ordner mit dem gleichen Namen in der gleichen �bergeordneten erfordern. 
  
Ein Suchordner enth�lt Links zu Nachrichten, die eine Reihe von vordefinierten Kriterien entsprechen. Da Suchordner Links anstelle von tats�chlichen Nachrichten enthalten, werden sie in Kraft schreibgesch�tzt. Nicht enthalten andere Ordner oder Nachrichten oder Ordner verschoben oder in diese kopiert. Sie d�rfen keine neue Nachrichten erstellt, in denen besitzen. und sie selbst verschoben, kopiert oder umbenannt werden nicht m�glich. Wenn eine Nachricht aus einem Suchordner gel�scht wird, wird sie tats�chlich aus dem Ordner gel�scht, die die Nachricht enth�lt.
  
Der Ordnertyp wird in der **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md)) -Eigenschaft gespeichert. Jeder Ordner hat diese Eigenschaft auf FOLDER_GENERIC, FOLDER_ROOT oder FOLDER_SEARCH, je nachdem dieses Typs festgelegt.
  
Jeder Ordner verf�gt �ber eine Eintrags-ID und einen Datensatzschl�ssel. Der **Eintragsbezeichner** PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) wird von Clients und Dienstanbietern zum Öffnen des Ordners verwendet. Der Datensatzschlüssel, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), ist ein binärer Wert, der zum Vergleichen des Ordners mit anderen Ordnern verwendet wird. 
  
Ein Ordner hat andere Eigenschaften zugeh�rigen Ordner und den Nachrichtenspeicher zu identifizieren. Die folgenden Eigenschaften sind erforderlich:
  
- **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))
    
- **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))
    
- **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))
    
Einige Ordner unterstützen die **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) -Eigenschaft, die den Typ der Vorgänge beschreibt, die ein Benutzer ausführen kann. Beispielsweise ist eine der g�ltigen Einstellungen f�r **PR_ACCESS** MAPI_ACCESS_DELETE, die angibt, dass der Ordner entfernt werden kann. Eine weitere Einstellung, MAPI_ACCESS_MODIFY, gibt an, dass der Ordner ge�ndert werden. 
  
Eine vollst�ndige Liste der erforderlichen Ordnereigenschaften finden Sie unter der [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Anwendungsentwicklung](mapi-application-development.md)

