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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347803"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen XML-Stream (Extensible Markup Language) zurück, der Informationen darstellt, die aus dem AutoErmittlungsdienst eines Microsoft Exchange 2007-Servers abgerufen wurden.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |olmapi32.dll  <br/> |
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
  
> [in] Eine SMTP-E-Mail-Adresse (Simple Mail Transfer Protocol, Simple Mail Transfer Protocol) des Kontos, für das Sie die Informationen zur automatischen Ermittlung abrufen möchten.
    
 _pwzPassword_
  
> [in] Ein optionales Kennwort für das von _pwzAddress angegebene Konto._ Beachten Sie, dass das Übergeben eines Kennworts keine Auswirkung hat, wenn für das von  _pwzAddress_ angegebene Konto kein Kennwort erforderlich ist. 
    
 _hCancelEvent_
  
> [in] Ein nicht verwendetes Win32-Ereignishandle, das optional ist und zum Abbrechen des Vorgangs verwendet werden kann. Zum Abbrechen des Vorgangs legen Sie das Ereignis fest, und übergeben Sie das Ereignishandle als  _hCancelEvent_; übergeben **Sie null,** wenn Sie den Vorgang nicht abbrechen möchten. Beachten Sie, dass das Übergeben eines Werts, der kein Ereignishandle repräsentiert, keine Auswirkung hat und von der Funktion ignoriert wird. 
    
 _ulFlags_
  
> [in] Dieser Parameter wird nicht verwendet. Es muss 0 sein.
    
 _ppXmlStream_
  
> [out] Ein Zeiger auf ein [IStream-Objekt,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) das die AutoErmittlungs-XML enthält. Gibt **null zurück,** wenn der AutoErmittlungsvorgang fehlschlägt. Sie müssen das [IStream-Objekt](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) los, wenn Sie damit fertig sind. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK 
  
- Der Funktionsaufruf ist erfolgreich.
    
E_INVALIDARG 
  
-  _pwzAddress_ ist **null** oder ist keine gültige SMTP-Adresse, oder _ppXmlStream_ ist ein **Nullzeiger** auf ein [IStream-Objekt.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 
    
MAPI_E_NOT_FOUND 
  
- Der Clientcomputer ist nicht mit dem Netzwerk verbunden, der Clientcomputer ist nicht mit einem Microsoft Exchange 2007-Server verbunden, _pwzAddress_ ist kein Konto auf einem Exchange 2007-Server, oder _pwzAddress_ ist ein Konto, das Exchange auto-discovery service nicht unterstützt. 
    
MAPI_E_USER_CANCEL 
  
- Ein Ereignishandle wurde an  _hCancelEvent übergeben,_ um den Vorgang abbricht. 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- Der an  _pwzAddress_ oder  _pwzPassword_ übergebene Wert ist zu lang, so dass er den internen Puffer der Größe 256 Byte überschreitet. 
    

