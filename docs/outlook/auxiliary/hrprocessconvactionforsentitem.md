---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Führt eine Kategorisierung nach dem Senden für ein E-Mail-Element basierend auf seiner PidTagConversationId aus.
ms.openlocfilehash: 45f1aa9dbab683fb6765d637b8495d77d899fbe2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614454"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

Führt eine Kategorisierung nach dem Senden für ein E-Mail-Element basierend auf seiner [PidTagConversationId aus.](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx)
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |Outlook.exe  <br/> |
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
  
> [in] Die [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) des Speichers oder die [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) des E-Mail-Elements. Darf nicht NULL oder ungültig sein. 
    
_pmbinMsgEid_
  
> [in] Die [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) des E-Mail-Elements. Darf nicht NULL oder ungültig sein. 
    
_pmbinConvID_
  
> [in] Die [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) des E-Mail-Elements. Darf nicht NULL oder ungültig sein. 
    
_Dwflags_
  
> [in] Eine Bitmaske, die zusätzliche Informationen zum Methodenaufruf angibt.
    
   - 0 – In diesem Methodenaufruf werden keine zusätzlichen Optionen verwendet. Dies ist der empfohlene Wert. 
    
   - **PCAFSIF_MSGEID_IS_SEARCH_KEY**- _pmbinMsgEid_ ist tatsächlich der [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) der Nachricht. Die Verwendung eines **PidTagSearchKey** ist ressourcenintensiv und sollte vermieden werden, wenn eine [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) verfügbar ist. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Anruf war erfolgreich.  <br/> |
|E_INVALIDARG  <br/> | _wetterflags_ enthält ein unbekanntes Kennzeichen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Kategorien werden als persönliche Informationen betrachtet und sollten nicht außerhalb des Postfachs des Benutzers übertragen werden. Rufen Sie daher **HrProcessConvActionForSentItem** nicht für ein nicht gesendetes E-Mail-Element auf. Senden Sie stattdessen das Element, und rufen Sie dann **HrProcessConvActionForSentItem** für die archivierte Kopie auf. Die archivierte Kopie kann im Ordner "Gesendete Elemente" oder an einem entsprechenden Speicherort gespeichert werden. 
  
Ihre Anwendung muss mit Outlook.exe verarbeitet werden, z. B. aus einem COM-Add-In, um **HrProcessConvActionForSentItem** aufzurufen. Wenn Sie versuchen, **HrProcessConvActionForSentItem** außerhalb des Prozesses aufzurufen, löst **HrProcessConvActionForSentItem** eine Zugriffsverletzungsausnahme aus. 
  

