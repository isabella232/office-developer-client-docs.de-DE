---
title: Hierarchietabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8aa6b36-d6e5-4e1f-8ac5-5d6a78a70bf8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2a1461f0c7196cd425d9736f5837b742bedd4fb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428368"
---
# <a name="hierarchy-tables"></a>Hierarchietabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Hierarchietabelle enthält Informationen zu den Ordnern in einem Nachrichtenspeicher oder zu den Containern in einem Adressbuchcontainer. Jede Zeile einer Hierarchietabelle enthält eine Reihe von Spalten mit Informationen zu einem Ordner oder Adressbuchcontainer. Hierarchietabellen werden in erster Linie von Clients verwendet und von Nachrichtenspeicheranbietern implementiert, um eine Struktur aus Ordnern und Unterordnern zu zeigen und von Adressbuchanbietern implementiert, um eine Struktur von Containern im Adressbuch zu zeigen. Container, die keine Untercontainer enthalten können, wie durch das Fehlen des AB_SUBCONTAINERS-Flags in ihrer **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))-Eigenschaft angegeben, implementieren keine Hierarchietabelle.
  
Auf eine Hierarchietabelle kann durch Aufrufen zugegriffen werden:
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - Oder -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) übergeben **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) als Eigenschaftstag und IID_IMAPITable als Schnittstellenbezeichner.
    
Container und Ordner müssen beide Techniken zum Abrufen von Tabelleneigenschaften unterstützen. Es ist nicht hinnehmbar, dass Dienstanbieter nur eine Möglichkeit für den Zugriff auf diese Tabellen unterstützen, da Clients erwarten, dass sie die Wahl haben. 
  
> [!IMPORTANT]
> Store Anbieter sind nicht garantiert, den für Hierarchietabellen angegebenen Sortierreihenfolgensatz zu honorieren. 
  
Der Aufruf von **IMAPIProp::OpenProperty** umfasst den Zugriff auf die Hierarchietabelle durch Öffnen der entsprechenden Eigenschaft, **PR_CONTAINER_HIERARCHY**. Obwohl **PR_CONTAINER_HIERARCHY** nicht über die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) eines Ordners oder Containers abgerufen werden kann, ist sie im Eigenschaftentagarray enthalten, das von der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) zurückgegeben wird. 
  
 **PR_CONTAINER_HIERARCHY** kann auch zum Ein- oder Ausschließen einer Hierarchietabelle aus einem Kopiervorgang verwendet werden. Wenn ein Client PR_CONTAINER_HIERARCHY im *lpExcludeProps-Parameter* für [IMAPIProp::CopyTo](imapiprop-copyto.md) in einem Kopiervorgang angibt, unterstützt der neue Ordner oder Container die Hierarchietabelle des ursprünglichen **Ordners** oder Containers nicht. 
  
Die folgenden Eigenschaften stellen den erforderlichen Spaltensatz in einer Hierarchietabelle zusammen:
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** enthält den Namen für den Container oder Ordner, der in der Anzeige der Hierarchie angezeigt werden soll. 
  
 **PR_ENTRYID** ist der Eintragsbezeichner, der diesem Container oder Ordner zugeordnet ist. Es wird erwartet, dass es sich um eine langfristige Eintrags-ID handelt. Clients und MAPI können diesen Eintragsbezeichner an **OpenEntry** übergeben, um den Container oder Ordner zu öffnen und dessen Inhalt durch Aufrufen von [IMAPIContainer::GetContentsTable anzuzeigen.](imapicontainer-getcontentstable.md) 
  
 **PR_DEPTH** ist ein numerischer Wert, der die Einzugsebene für diesen Container oder Ordner angibt, bei dem Null die oberste Ebene ist. Je tiefer sich ein Container oder Ordner in der Hierarchie befindet, desto höher ist der Wert für **PR_DEPTH** Eigenschaft. Clients verwenden  die PR_DEPTH-Eigenschaft, um eine Hierarchietabelle entsprechend anzeigen zu können, damit Benutzer beziehungen zwischen übergeordneten und untergeordneten Benutzern deutlich sehen können. Die Container- oder Ordnertiefe ist immer relativ zum Container oder Ordner, der die Hierarchietabelle implementieren. 
  
 **PR_OBJECT_TYPE** ist immer auf MAPI_ABCONT für Adressbuchhierarchietabellen und MAPI_FOLDER Ordnerhierarchietabellen festgelegt. 
  
 **PR_DISPLAY_TYPE** ist ein numerischer Wert, der sich darauf bezieht, wie ein Container oder Ordner in der Hierarchietabelle angezeigt wird. Es wird hauptsächlich zu Anzeigezwecken verwendet, um visuell zwischen Typen von Containern oder Ordnern zu unterscheiden. Viele Nachrichtenspeicher- und Adressbuchanbieter verwenden Symbole für die verschiedenen Anzeigetypen. Es liegt an dem Anbieter, diese Symbole zu liefern. MAPI gibt keine Standardwerte an. 
  
MAPI definiert viele Werte für **PR_DISPLAY_TYPE**, einige, die für Ordner gültig sind, und andere, die mit den Hierarchietabellen von Adressbuchcontainern verwendet werden. In der Regel  ist die PR_DISPLAY_TYPE eines Ordners auf DT_FOLDER festgelegt, um ein Standardordnersymbol anzugeben, DT_FOLDER_LINK ein Symbol anzugeben, das einen Link zu einem anderen Ordner darstellt, oder DT_FOLDER_SPECIAL, um ein anwendungsspezifisches Symbol anzugeben. DT_FOLDER_LINK wird mit Suchergebnissenordnern verwendet. 
  
Zusätzlich zu diesen erforderlichen Spalten müssen Adressbuchhierarchietabellen die PR_CONTAINER_FLAGS **enthalten.** **PR_CONTAINER_FLAGS** gibt verschiedene Attribute zu einem Container in der Hierarchie an und wird verwendet, um einen Container von einem anderen zu unterscheiden. 
  
Eine optionale Eigenschaft für Adressbuchhierarchietabellen ist die **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) -Eigenschaft.
  
Die Hierarchietabellen des Nachrichtenspeichers enthalten diese Eigenschaften in ihrem erforderlichen Spaltensatz:
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
Adressbuchanbieter müssen die folgenden **IMAPITable-Methoden** in ihren Hierarchietabellenimplementierung unterstützen, da sie vom integrierten Adressbuch MAPI benötigt werden: 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

