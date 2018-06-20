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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8b6d4fa1d9ffa6ab5f800bad9f02ac5aa9abd8c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791942"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**Betrifft**: Outlook 
  
Einen Nachrichtenspeicher hinzugefügt standard zwischen Personen (IPM) Nachrichtenordner. 
  
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
  
> [in] Zeiger auf die Nachricht speichern-Objekt, dem der Ordner hinzufügen. 
    
 _ulFlags_
  
> [in] Bitmaske aus Flags verwendet, um zu steuern, wie die Ordner erstellt werden. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_FORCE_CREATE 
  
> Die Ordner sollte vor dem Erstellen der, überprüft werden, selbst wenn die Eigenschaften des Nachrichtenspeichers Geben Sie an, dass sie gültig sind. Eine Clientanwendung wird dieses Flag in der Regel, wenn ein Fehler weist darauf hin, dass die Struktur eines vorhandenen Ordners beschädigt ist. 
    
MAPI_FULL_IPM_TREE 
  
> Der vollständige Satz IPM Ordner sollte im Stammordner der Nachrichtenspeicher erstellt werden. Der Ordner Titel in der Hierarchie sind:
    
    - Ordneransichten
    
    - Allgemeine Ansichten
    
    - Stamm der Suche\*
    
    - IPM-Unterstruktur\*
    
    - Posteingang
    
    - Postausgang
    
    - Gelöschte Elemente\*
    
    - Gesendete Elemente
    
    die drei Ordner, in dem mit markiert \* werden den Mindestsatz erstellt, auch wenn das Flag MAPI_FULL_IPM_TREE nicht festgelegt wurde. Eine Clientanwendung wird dieses Flag in der Regel, wenn der Nachrichtenspeicher, in dem der Ordner sind zu erstellenden, des Standard-Informationsspeichers ist.
    
 _lpcValues_
  
> [in, out] Zeiger auf die Anzahl der [SPropValue](spropvalue.md) Strukturen in das im Parameter _LppProps_ zurückgegebene Array. Der Wert des Parameters _LpcValues_ kann 0 (null) sein, wenn _LppProps_ NULL ist. 
    
 _lppProps_
  
> [in, out] Zeiger auf einen Zeiger auf ein Array von **SPropValue** -Strukturen, Eigenschaftswerte für die Eigenschaft **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) und für die entsprechenden Ordner Eintrags-ID-Eigenschaften enthält. Wenn **HrValidateIPMSubtree** einen Posteingang im Nachrichtenspeicher erstellt, enthält das Array **SPropValue** ein Posteingang Eintrags-ID mit einem speziellen Eigenschaftentag als codierte `PROP_TAG(PT_BINARY, PROP_ID_NULL)`. Der Parameter _LppProps_ möglicherweise NULL-Wert zurück, der angibt, dass die aufrufende Implementierung nicht erfordert, dass ein **SPropValue** Array zurückgegeben werden. 
    
 _lppMapiError_
  
> [out] Zeiger auf einen Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur, die Angaben zu Version, Komponente und Kontext für einen Fehler enthält. Der Parameter _LppMAPIError_ ist auf NULL festgelegt, wenn keine **MAPIERROR** -Struktur zurückgegeben wird. 
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>Hinweise

MAPI verwendet die Funktion **HrValidateIPMSubtree** intern standard IPM-Unterstruktur in einem Nachrichtenspeicher erstellt wird, wenn der Informationsspeicher zum ersten Mal geöffnet wird, oder ein Speichers Standard speichern vorgenommen wird. Diese Funktion kann auch verwendet werden von Clientanwendungen überprüfen oder Reparatur von e-Mail-Ordnern. 
  
 **HrValidateIPMSubtree** wird immer die Suche Domänenstamm und in IPM-Unterstruktur Ordner im Stammordner des Speichers und der Ordner Gelöschte Elemente im Ordner "IPM-Unterstruktur" erstellt. Der Ordner IPM-Unterstruktur ist der Stamm der Hierarchie IPM in dieser Nachrichtenspeicher. Suche Stammordner kann als Basis für eine Unterstruktur für Suchergebnisse Ordner verwendet werden. 
  
IPM Clients sollte ihre Ordneransicht beginnend am IPM Unterstruktur Stammordner und Anzeigen von untergeordneten Ordner darunter angezeigt werden. Informationen in den Stammordner eines Nachrichtenspeichers sollte nicht in einem Client-Benutzeroberfläche angezeigt werden. Dies bedeutet, dass wenn ein Client Informationen ausblenden muss, die Informationen in das Stammverzeichnis IPM Unterstruktur versetzt werden kann, ist es nicht für den Benutzer sichtbar. Im Gegensatz dazu können sie nicht-IPM-Anwendungen, die Nachrichten und Ordnern für den Benutzer, beispielsweise in einem serverbasierten Nachrichtenspeicher, unsichtbar werden müssen, außerhalb der Hierarchie IPM platzieren. 
  
 **HrValidateIPMSubtree** wird die **PR_VALID_FOLDER_MASK** -Eigenschaft, um anzugeben, ob jeder IPM-Ordner erstellt werden, eine gültige Eingabe-ID hat. Die folgenden Eigenschaften des Nachrichtenspeichers Eintrag sind der entsprechenden Ordner auf den Eintrag festgelegt und im Parameter _LppProps_ zusammen mit **PR_VALID_FOLDER_MASK**zurückgegeben: 
  
 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> Ein Platzhalter [PROP_TAG](prop_tag.md) für den Posteingang IPM (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MstStoreDlg.cpp  <br/> |CMsgStoreDlg::OnValidateIPMSubtree  <br/> |MFCMAPI (engl.) verwendet die **HrValidateIPMSubtree** -Methode, um einen Nachrichtenspeicher standard Ordner hinzuzufügen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

