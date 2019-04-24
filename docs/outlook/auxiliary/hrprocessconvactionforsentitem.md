---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Führt die Kategorisierung nach dem Senden für ein e-Mail-Element basierend auf dessen PidTagConversationId aus.
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318900"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

Führt die Kategorisierung nach dem Senden für ein e-Mail-Element basierend auf dessen [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx)aus.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |Outlook. exe  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a>Parameter

_pmbinStoreEid_
  
> in Die [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) des Speichers oder die [pidtagstoreentryid (](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) des e-Mail-Elements. Darf nicht NULL oder ungültig sein. 
    
_pmbinMsgEid_
  
> in Die [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) des e-Mail-Elements. Darf nicht NULL oder ungültig sein. 
    
_pmbinConvID_
  
> in Die [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) des e-Mail-Elements. Darf nicht NULL oder ungültig sein. 
    
_dwFlags_
  
> in Eine Bitmaske, die zusätzliche Informationen über den Methodenaufruf angibt.
    
   - 0 – bei diesem Methodenaufruf werden keine weiteren Optionen verwendet. Dies ist der empfohlene Wert. 
    
   - **PCAFSIF_MSGEID_IS_SEARCH_KEY**– _pmbinMsgEid_ ist tatsächlich der [pidtagsearchkey (](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) der Nachricht. Die Verwendung eines **pidtagsearchkey (** ist ressourcenintensiv und sollte vermieden werden, wenn ein [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) verfügbar ist. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Anruf wurde erfolgreich ausgeführt.  <br/> |
|E_INVALIDARG  <br/> | _dwFlags_ enthält ein unbekanntes Flag.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Kategorien werden als persönliche Informationen betrachtet und sollten nicht außerhalb des Postfachs des Benutzers übertragen werden. Rufen Sie daher **HrProcessConvActionForSentItem** nicht für ein nicht gesendetes e-Mail-Element auf. Senden Sie stattdessen das Element, und rufen Sie dann **HrProcessConvActionForSentItem** für die archivierte Kopie auf. Die archivierte Kopie kann im Ordner "Gesendete Elemente" oder an einem entsprechenden Speicherort gespeichert werden. 
  
Ihre Anwendung muss mit Outlook. exe, beispielsweise aus einem COM-Add-in, in Bearbeitung sein, um **HrProcessConvActionForSentItem**aufzurufen. Wenn Sie versuchen, **HrProcessConvActionForSentItem** out-of-Process aufzurufen, löst **HrProcessConvActionForSentItem** eine Zugriffsverletzungsausnahme aus. 
  

