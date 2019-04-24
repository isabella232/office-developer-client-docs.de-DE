---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Erstellt ein Objekt, auf das ein Client in einem bevorzugten Zeichenformat zugreifen kann.
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317605"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

Erstellt ein Objekt, auf das ein Client in einem bevorzugten Zeichenformat zugreifen kann.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |msmapi32. dll  <br/> |
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
  
> in Das anfängliche nicht umbrochene Outlook-Objekt. Eine der folgenden Schnittstellen muss implementiert werden:
    
   - [IMailUser: IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder: IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage: IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore: IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon: IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx)oder [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).
    
_ulUnwrappedFlags_
  
> in Flags, die das nicht umbrochene anfängliche Objekt charakterisieren. Muss einer oder mehrere der folgenden Werte sein:
    
   - DDLWRAP_FLAG_ANSI – unwrapped-Objekt ist ANSI.
    
   - DDLWRAP_FLAG_UNICODE – unwrapped-Objekt ist UNICODE.
    
_ulWrappedFlags_
  
>  in Flags für das bevorzugte Zeichenformat. Muss einer oder mehrere der folgenden Werte sein: 
    
   - DDLWRAP_FLAG_ANSI – Wrapped-Objekt wird als ANSI verfügbar gemacht.
    
   - DDLWRAP_FLAG_UNICODE – Wrapped-Objekt wird als UNICODE verfügbar gemacht.
    
_pIID_
  
>  in Der Bezeichner der Schnittstelle, die vom unwrapped-Objekt unterstützt wird; Legen Sie ihn auf NULL fest, wenn dieser nicht bekannt ist. 
    
_pulReserved_
  
>  in Dieser Parameter wird nicht verwendet. Sie muss NULL sein. 
    
_fCheckWrap_
  
>  in Legen Sie diesen Parameter auf **true** fest, wenn _pvUnwrapped_ vor dem Umbruch auf sein Format überprüft werden soll; Legen Sie ihn auf **false** fest, wenn das Objekt ohne Überprüfung umbrochen werden soll. 
    
_ppvWrapped_
  
>  Out Ein Zeiger auf das angeforderte Objekt, das im angeforderten Zeichenformat eingeschlossen ist. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Bemerkungen

Das Übergeben eines eingebundenen Objekts mit _fCheckWrap_ , das auf **true** festgelegt ist, führt zu einem unwrapped-Objekt. Unabhängig davon, ob das zurückgegebene Objekt umbrochen wird, ist der Client für die Freigabe des Verweises auf das zurückgegebene Objekt verantwortlich. 
  
Wenn Sie **GetProcAddress** verwenden, um nach der Adresse dieser Funktion in msmapi32. dll zu suchen, geben Sie **HrCreateNewWrappedObject @ 28** als Prozedurnamen an. 
  
## <a name="see-also"></a>Siehe auch

- [Über der Datenschicht Abbau API](about-the-data-degradation-layer-api.md)
- [Konstanten (Daten Degradations Schicht-API)](constants-data-degradation-layer-api.md)

