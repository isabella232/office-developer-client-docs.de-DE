---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Führt eine Post-Send-Kategorisierung für ein E-Mail-Element basierend auf seiner PidTagConversationId durch.
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318900"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

Führt die Post-Send-Kategorisierung für ein E-Mail-Element basierend auf seiner [PidTagConversationId aus.](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx)
  
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
  
> [in] Die [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) des Speichers oder [die PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) des E-Mail-Elements. Kann nicht NULL oder ungültig sein. 
    
_pmbinMsgEid_
  
> [in] Die [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) des E-Mail-Elements. Kann nicht NULL oder ungültig sein. 
    
_pmbinConvID_
  
> [in] Die [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) des E-Mail-Elements. Kann nicht NULL oder ungültig sein. 
    
_dwFlags_
  
> [in] Eine Bitmaske, die zusätzliche Informationen zum Methodenaufruf angibt.
    
   - 0 – In diesem Methodenaufruf werden keine zusätzlichen Optionen verwendet. Dies ist der empfohlene Wert. 
    
   - **PCAFSIF_MSGEID_IS_SEARCH_KEY**– _pmbinMsgEid_ ist tatsächlich [der PidTagSearchKey der](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) Nachricht. Die Verwendung **eines PidTagSearchKey** ist ressourcenintensiv und sollte vermieden werden, wenn [eine PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) verfügbar ist. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_INVALIDARG  <br/> | _dwFlags_ enthält ein unbekanntes Flag.  <br/> |
   
## <a name="remarks"></a>Hinweise

Kategorien gelten als persönliche Informationen und sollten nicht außerhalb des Postfachs des Benutzers übermittelt werden. Rufen Sie daher **hrProcessConvActionForSentItem** nicht für ein nicht gesendetes E-Mail-Element auf. Senden Sie stattdessen das Element, und rufen Sie **dann HrProcessConvActionForSentItem** für die archivierte Kopie auf. Die archivierte Kopie kann im Ordner "Gesendete Elemente" oder an einem entsprechenden Speicherort gespeichert werden. 
  
Ihre Anwendung muss mit Outlook.exe, z. B. von einem COM-Add-In, in Prozess sein, um **HrProcessConvActionForSentItem aufrufen** zu können. Wenn Sie versuchen, **HrProcessConvActionForSentItem** nicht mehr zu verarbeiten, wird von **HrProcessConvActionForSentItem** eine Zugriffsverletzungsausnahme ausgelöst. 
  

