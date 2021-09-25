---
title: Hierarchietabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b8aa6b36-d6e5-4e1f-8ac5-5d6a78a70bf8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 59e348784d0170fa087e62b353c77188c6c8631c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556651"
---
# <a name="hierarchy-tables"></a>Hierarchietabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Hierarchietabelle enthält Informationen zu den Ordnern in einem Nachrichtenspeicher oder zu den Containern in einem Adressbuchcontainer. Jede Zeile einer Hierarchietabelle enthält eine Reihe von Spalten mit Informationen zu einem Ordner oder Adressbuchcontainer. Hierarchietabellen werden in erster Linie von Clients verwendet und von Nachrichtenspeicheranbietern implementiert, um eine Struktur von Ordnern und Unterordnern anzuzeigen, und von Adressbuchanbietern implementiert, um eine Struktur von Containern im Adressbuch anzuzeigen. Container, die keine Untercontainer enthalten können, wie durch das Fehlen des AB_SUBCONTAINERS Flags in ihrer **eigenschaft PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) angegeben, implementieren keine Hierarchietabelle.
  
Sie können auf eine Hierarchietabelle zugreifen, indem Sie Folgendes aufrufen:
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - Oder -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) passing **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) as the property tag and IID_IMAPITable as the interface identifier.
    
Container und Ordner müssen beide Techniken zum Abrufen von Tabelleneigenschaften unterstützen. Es ist inakzeptabel, dass Dienstanbieter nur eine Möglichkeit zum Zugriff auf diese Tabellen unterstützen, da Clients davon ausgehen, dass sie die Wahl haben. 
  
> [!IMPORTANT]
> Store Anbieter nicht garantiert, dass sie den für Hierarchietabellen angegebenen Sortierreihenfolgesatz berücksichtigen. 
  
Der Aufruf von **IMAPIProp::OpenProperty** umfasst den Zugriff auf die Hierarchietabelle, indem die entsprechende Eigenschaft **PR_CONTAINER_HIERARCHY** geöffnet wird. Obwohl **PR_CONTAINER_HIERARCHY** nicht über die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) eines Ordners oder Containers abgerufen werden kann, ist sie im Eigenschaftentagarray enthalten, das von der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) zurückgegeben wird. 
  
 **PR_CONTAINER_HIERARCHY** können auch verwendet werden, um eine Hierarchietabelle in einen Kopiervorgang einzuschließen oder auszuschließen. Wenn ein Client **PR_CONTAINER_HIERARCHY** im  *LpExcludeProps-Parameter*  für [IMAPIProp::CopyTo](imapiprop-copyto.md) in einem Kopiervorgang angibt, unterstützt der neue Ordner oder Container die Hierarchietabelle des ursprünglichen Ordners oder Containers nicht. 
  
Die folgenden Eigenschaften bilden den erforderlichen Spaltensatz in einer Hierarchietabelle:
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** enthält den Namen des Containers oder Ordners, der in der Anzeige der Hierarchie angezeigt werden soll. 
  
 **PR_ENTRYID** ist der Eintragsbezeichner, der diesem Container oder Ordner zugeordnet ist. Es wird erwartet, dass es sich um einen langfristigen Eintragsbezeichner handelt. Clients und MAPI können diesen Eintragsbezeichner an **OpenEntry** übergeben, um den Container oder Ordner zu öffnen und seine Inhalte anzuzeigen, indem [sie IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)aufrufen. 
  
 **PR_DEPTH** ist ein numerischer Wert, der die Einzugsebene für diesen Container oder Ordner angibt, wobei Null die oberste Ebene ist. Je tiefer in der Hierarchie sich ein Container oder Ordner befindet, desto höher ist der Wert für seine **PR_DEPTH** Eigenschaft. Clients verwenden  die PR_DEPTH-Eigenschaft, um eine Hierarchietabelle entsprechend anzuzeigen, damit Benutzer beziehungen zwischen übergeordneten und untergeordneten Elementen deutlich sehen können. Die Container- oder Ordnertiefe ist immer relativ zum Container oder Ordner, der die Hierarchietabelle implementiert. 
  
 **PR_OBJECT_TYPE** wird immer auf MAPI_ABCONT für Adressbuchhierarchietabellen und MAPI_FOLDER für Ordnerhierarchietabellen festgelegt. 
  
 **PR_DISPLAY_TYPE** ist ein numerischer Wert, der sich darauf bezieht, wie ein Container oder Ordner in der Hierarchietabelle angezeigt wird. Es wird hauptsächlich für Anzeigezwecke verwendet, um visuell zwischen Containertypen oder Ordnern zu unterscheiden. Viele Nachrichtenspeicher- und Adressbuchanbieter verwenden Symbole für die verschiedenen Anzeigetypen. Es liegt an dem Anbieter, diese Symbole zu liefern. MapI stellt keine Standardwerte zur Verfügung. 
  
MAPI definiert viele Werte für **PR_DISPLAY_TYPE,** einige für Ordner und andere, die mit den Hierarchietabellen von Adressbuchcontainern verwendet werden. In der Regel wird die **PR_DISPLAY_TYPE** eines Ordners auf DT_FOLDER festgelegt, um ein Standardordnersymbol anzugeben, DT_FOLDER_LINK, um ein Symbol anzugeben, das einen Link zu einem anderen Ordner darstellt, oder DT_FOLDER_SPECIAL, um ein anwendungsspezifisches Symbol anzugeben. DT_FOLDER_LINK wird mit Suchergebnisordnern verwendet. 
  
Zusätzlich zu diesen erforderlichen Spalten müssen Adressbuchhierarchietabellen die **PR_CONTAINER_FLAGS-Eigenschaft** enthalten. **PR_CONTAINER_FLAGS** gibt verschiedene Attribute zu einem Container in der Hierarchie an und wird verwendet, um einen Container von einem anderen zu unterscheiden. 
  
Eine optionale Eigenschaft für Adressbuchhierarchietabellen ist die **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) -Eigenschaft.
  
Hierarchietabellen für Nachrichtenspeicher enthalten diese Eigenschaften in ihrem erforderlichen Spaltensatz:
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
Adressbuchanbieter müssen die folgenden **IMAPITable-Methoden** in ihren Hierarchietabellenimplementierungen unterstützen, da sie für das integrierte MAPI-Adressbuch erforderlich sind: 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

