---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436573"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt einem Nachrichtenspeicher standardmäßige IPM-Ordner (Interpersonal Message) hinzu. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a>Parameter

 _lpMDB_
  
> [in] Zeiger auf das Nachrichtenspeicherobjekt, dem die Ordner hinzugefügt werden. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die verwendet werden, um zu steuern, wie die Ordner erstellt werden. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_FORCE_CREATE 
  
> Die Ordner sollten vor der Erstellung überprüft werden, auch wenn Nachrichtenspeichereigenschaften angeben, dass sie gültig sind. Eine Clientanwendung legt dieses Flag in der Regel fest, wenn ein Fehler darauf hinweist, dass die Struktur eines vorhandenen Ordners beschädigt wurde. 
    
MAPI_FULL_IPM_TREE 
  
> Der vollständige Satz von IPM-Ordnern sollte im Stammordner des Nachrichtenspeichers erstellt werden. Die Ordnertitel in der Hierarchie sind:
    
    - Ordneransichten
    
    - Allgemeine Ansichten
    
    - Suchstamm\*
    
    - IPM-Unterstruktur\*
    
    - Posteingang
    
    - Postausgang
    
    - Gelöschte Elemente\*
    
    - Gesendete Elemente
    
    dabei sind die drei mit markierten Ordner die Mindestanzahl, die auch dann erstellt wird, wenn das MAPI_FULL_IPM_TREE nicht \* festgelegt wurde. Eine Clientanwendung legt dieses Flag in der Regel fest, wenn der Nachrichtenspeicher, in dem die Ordner erstellt werden sollen, der Standardspeicher ist.
    
 _lpcValues_
  
> [in, out] Zeiger auf die Anzahl [der SPropValue-Strukturen](spropvalue.md) im Array, das im  _lppProps-Parameter zurückgegeben_ wird. Der Wert des  _lpcValues-Parameters_ kann null sein, wenn  _lppProps_ NULL ist. 
    
 _lppProps_
  
> [in, out] Zeiger auf einen Zeiger auf ein Array von **SPropValue-Strukturen,** das Eigenschaftswerte für die **PR_VALID_FOLDER_MASK** -[PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)-Eigenschaft und für die entsprechenden Eigenschaften der Ordnereintrags-ID enthält. Wenn **HrValidateIPMSubtree** einen Posteingang im Nachrichtenspeicher erstellt, enthält das **SPropValue-Array** einen Posteingangseintragsbezeichner mit einem speziellen Eigenschaftstag, das als codiert  `PROP_TAG(PT_BINARY, PROP_ID_NULL)` ist. Der  _lppProps-Parameter_ kann NULL sein, was angibt, dass für die aufrufende Implementierung kein **SPropValue-Array** zurückgegeben werden muss. 
    
 _lppMapiError_
  
> [out] Zeiger auf einen Zeiger auf eine [MAPIERROR-Struktur,](mapierror.md) die Versions-, Komponenten- und Kontextinformationen für einen Fehler enthält. Der  _lppMAPIError-Parameter_ ist auf NULL festgelegt, wenn keine **MAPIERROR-Struktur** zurückgegeben wird. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

MAPI verwendet die **HrValidateIPMSubtree-Funktion** intern, um die standardmäßige IPM-Unterstruktur in einem Nachrichtenspeicher zu erstellen, wenn der Speicher zum ersten Mal geöffnet wird oder wenn ein Speicher zum Standardspeicher gemacht wird. Diese Funktion kann auch von Clientanwendungen verwendet werden, um Standardnachrichtenordner zu überprüfen oder zu reparieren. 
  
 **HrValidateIPMSubtree** erstellt immer die Ordner Suchstamm und IPM-Unterstruktur im Stammordner des Speichers und den Ordner Gelöschte Elemente im Ordner "IPM Subtree". Der Ordner "IPM-Unterstruktur" ist der Stamm der IPM-Hierarchie in diesem Nachrichtenspeicher. Der Ordner "Suchstamm" kann als Stamm einer Unterstruktur für Suchergebnisordner verwendet werden. 
  
IPM-Clients sollten ihre Ordneransicht ab dem Stammordner der IPM-Unterstruktur und untergeordnete Ordner darunter anzeigen. Informationen im Stammordner eines Nachrichtenspeichers sollten nicht auf der Benutzeroberfläche eines Clients angezeigt werden. Diese Funktionalität bedeutet, dass, wenn ein Client Informationen ausblenden muss, die Informationen im Stammverzeichnis der IPM-Unterstruktur gespeichert werden können, wo sie für den Benutzer nicht sichtbar sind. Im Gegensatz dazu können Nicht-IPM-Anwendungen, bei denen Nachrichten und Ordner für den Benutzer unsichtbar sein müssen, z. B. in einem serverbasierten Nachrichtenspeicher, diese außerhalb der IPM-Hierarchie setzen. 
  
 **HrValidateIPMSubtree** legt die **PR_VALID_FOLDER_MASK** fest, um anzugeben, ob jeder erstellte IPM-Ordner über einen gültigen Eintragsbezeichner verfügt. Die folgenden Eintragsbezeichnereigenschaften des Nachrichtenspeichers werden auf die Eintragsbezeichner der entsprechenden Ordner festgelegt und zusammen mit dem Parameter _"lppProps"_ **PR_VALID_FOLDER_MASK:** 
  
 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> Ein Platzhalter [PROP_TAG](prop_tag.md) für den IPM-Posteingang (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MstStoreDlg.cpp  <br/> |CMsgStoreDlg::OnValidateIPMSubtree  <br/> |MFCMAPI verwendet die **HrValidateIPMSubtree-Methode,** um Einem Nachrichtenspeicher Standardordner hinzuzufügen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

