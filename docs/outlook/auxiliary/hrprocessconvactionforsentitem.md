---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Dient zum Senden nach der Kategorisierung auf ein e-Mail-Element basierend auf der PidTagConversationId.
ms.openlocfilehash: efecfc2d0d865428cb958fc15a858bbc7807c5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790954"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

Dient zum Senden nach der Kategorisierung auf ein e-Mail-Element basierend auf der [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Vom exportiert werden:  <br/> |Outlook.exe  <br/> |
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
  
> [in] Die [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) der im Store oder der [PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) des e-Mail-Elements. Kann nicht NULL sein oder ungültig. 
    
_pmbinMsgEid_
  
> [in] Die [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) des e-Mail-Elements. Kann nicht NULL sein oder ungültig. 
    
_pmbinConvID_
  
> [in] Die [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) des e-Mail-Elements. Kann nicht NULL sein oder ungültig. 
    
_dwFlags_
  
> [in] Eine Bitmaske, die zusätzliche Informationen über den Aufruf der Methode angibt.
    
   - 0 – keine zusätzlichen Optionen in diesem Methodenaufruf verwendet werden. Dies ist der empfohlene Wert. 
    
   - **PCAFSIF_MSGEID_IS_SEARCH_KEY**– _PmbinMsgEid_ ist tatsächlich [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) der Nachricht. Verwenden einer **PidTagSearchKey** ressourcenintensiv und sollte vermieden werden, wenn eine [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) verfügbar ist. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_INVALIDARG  <br/> | _DwFlags_ enthält eine unbekannte Kennzeichnung.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Kategorien werden persönlichen Informationen berücksichtigt und sollten nicht außerhalb des Postfachs des Benutzers übermittelt werden. Rufen Sie daher nicht **HrProcessConvActionForSentItem** für ein Element nicht gesendeten Nachrichten. Stattdessen senden Sie des Elements, und rufen Sie dann auf der archivierten **HrProcessConvActionForSentItem** . Der archivierten kann in den Ordner Gesendete Objekte oder einen entsprechenden Speicherort gespeichert werden. 
  
Ihre Anwendung muss in-Process mit Outlook.exe, z. B. von einem COM-add-in, **HrProcessConvActionForSentItem**aufrufen. Wenn Sie versuchen, **HrProcessConvActionForSentItem** Out-of-Process aufrufen, wird **HrProcessConvActionForSentItem** eine zugriffsverletzung Ausnahme ausgelöst. 
  

