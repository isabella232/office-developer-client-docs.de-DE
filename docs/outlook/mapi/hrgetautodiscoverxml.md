---
title: HrGetAutoDiscoverXML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 77f28654ffe0f6f459fde229bb7428f2c39e96c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400719"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Stream Extensible Markup Language (XML), der Informationen aus den Auto-Discovery-Dienst eines Microsoft Exchange 2007-Servers abgerufen darstellt zurück.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Vom exportiert werden:  <br/> |olmapi32.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a>Parameter

 _pwzAddress_
  
> [in] Eine Null endende Simple Mail Transfer Protocol (SMTP) e-Mail-Adresse des Kontos ein, für die Sie die automatische Ermittlung Informationen abrufen möchten.
    
 _pwzPassword_
  
> [in] Ein optionales Kennwort für das Konto durch _PwzAddress_angegeben. Beachten Sie, dass jedes beliebige Kennwort übergeben hat keine Auswirkung, wenn das durch _PwzAddress_ angegebene Konto ein Kennwort nicht erforderlich sind. 
    
 _hCancelEvent_
  
> [in] Ein nicht festgelegte Win32-Ereignishandle, das ist optional und kann verwendet werden, um den Vorgang abzubrechen. Um den Vorgang abzubrechen, legen Sie das Ereignis, und übergeben Sie das Ereignishandle als _hCancelEvent_; übergeben Sie **null** , wenn Sie nicht, um den Vorgang abzubrechen möchten. Beachten Sie, dass ein Wert übergeben, die ein Ereignishandle nicht darstellen hat keine Auswirkung und wird von der Funktion ignoriert. 
    
 _ulFlags_
  
> [in] Dieser Parameter wird nicht verwendet. Es muss 0 sein.
    
 _ppXmlStream_
  
> [out] Ein Zeiger auf ein [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Objekt, das die AutoErmittlung XML enthält. Gibt **null** zurück, wenn der AutoErmittlung-Vorgang fehlschlägt. Wenn Sie mit ihm fertig sind, müssen Sie [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Objekt freigeben. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK 
  
- Der Funktionsaufruf ist erfolgreich.
    
E_INVALIDARG 
  
-  _PwzAddress_ ist **null** oder ist keine gültige SMTP-Adresse, oder _PpXmlStream_ ist ein **null** -Zeiger auf eine [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Objekt. 
    
MAPI_E_NOT_FOUND 
  
- Clientcomputer ist nicht mit dem Netzwerk verbunden, Client-Computer ist nicht mit einem Microsoft Exchange 2007-Server verbunden, _PwzAddress_ ist nicht mit einem Konto auf einem Exchange 2007-Server oder _PwzAddress_ ist ein Konto, das Exchange nicht unterstützt Auto-Discovery-Dienst. 
    
MAPI_E_USER_CANCEL 
  
- Ein Ereignishandle wurde übergeben, _hCancelEvent_ , um den Vorgang abzubrechen. 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- Der _PwzAddress_ oder _PwzPassword_ übergebene Wert ist zu lang, so, dass er den internen Puffer Größe 256 Bytes überschreitet. 
    

