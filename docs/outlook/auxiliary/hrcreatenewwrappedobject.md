---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Erstellt ein Objekt, das ein Client zugreifen kann in einem bevorzugten Zeichenformat.
ms.openlocfilehash: 187bcbce8fd1170e05f57c5c9147a8962669fea4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790942"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

Erstellt ein Objekt, das ein Client zugreifen kann in einem bevorzugten Zeichenformat.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Vom exportiert werden:  <br/> |Msmapi32.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT HrCreateNewWrappedObject( 
    LPVOID        pvUnwrapped, 
    ULONG         ulUnwrappedFlags, 
    ULONG         ulWrappedFlags, 
    const IID     *pIID, 
    const ULONG   *pulReserved, 
    BOOL          fCheckWrap, 
    LPVOID       *ppvWrapped 
);

```

## <a name="parameters"></a>Parameter

_pvUnwrapped_
  
> [in] Das ursprüngliche allein stehenden Outlook-Objekt. Muss eine der folgenden Schnittstellen implementieren:
    
   - [IMailUser: IMAPIProp](http://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder: IMAPIContainer](http://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage: IMAPIProp](http://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore: IMAPIProp](http://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon: IUnknown](http://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), oder [IOSTX](http://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).
    
_ulUnwrappedFlags_
  
> [in] Kennzeichen, die das ursprüngliche allein stehenden Objekt charakterisiert wird. Eine oder mehrere der folgenden Werte muss sein:
    
   - DDLWRAP_FLAG_ANSI – Unwrapped-Objekt ist ANSI.
    
   - DDLWRAP_FLAG_UNICODE – Unwrapped-Objekt ist UNICODE.
    
_ulWrappedFlags_
  
>  [in] Flags für die bevorzugten Zeichenformat. Eine oder mehrere der folgenden Werte muss sein: 
    
   - DDLWRAP_FLAG_ANSI – Wrapped-Objekt wird als ANSI verfügbar gemacht werden.
    
   - DDLWRAP_FLAG_UNICODE – Wrapped-Objekt wird als UNICODE verfügbar gemacht werden.
    
_pIID_
  
>  [in] Der Bezeichner der Schnittstelle, durch die allein stehenden-Objekt unterstützt; Legen Sie es auf NULL, wenn dies nicht bekannt ist. 
    
_pulReserved_
  
>  [in] Dieser Parameter wird nicht verwendet. Es muss NULL sein. 
    
_fCheckWrap_
  
>  [in] Legen Sie diesen Parameter auf **true fest,** Wenn _PvUnwrapped_ auf seinem Format vor Umbruch überprüft werden soll; Legen Sie ihn auf **false fest** , wenn das Objekt ohne Überprüfung umbrochen werden soll. 
    
_ppvWrapped_
  
>  [out] Ein Zeiger auf das angeforderte Objekt, in das angeforderte Zeichenformat eingeschlossen. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Anmerkungen

Ein Objekt allein stehenden führt übergeben in einem gepackten-Objekt mit _fCheckWrap_ auf **true** festgelegt. Unabhängig davon, ob das zurückgegebene Objekt umgebrochen wird muss der Client für den Verweis auf das zurückgegebene Objekt freigeben. 
  
Wenn **GetProcAddress** für die Adresse des dieser Funktion in msmapi32.dll suchen, geben Sie **HrCreateNewWrappedObject@28** als den Namen der Prozedur. 
  
## <a name="see-also"></a>Siehe auch

- [Über der Datenschicht Abbau API](about-the-data-degradation-layer-api.md)
- [Konstanten (Beeinträchtigung Datenebene API)](constants-data-degradation-layer-api.md)

