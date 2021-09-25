---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Erstellt ein Objekt, auf das ein Client in einem bevorzugten Zeichenformat zugreifen kann.
ms.openlocfilehash: 7832b495e8d5e7ee1849782269f073fd4fa28392
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552087"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

Erstellt ein Objekt, auf das ein Client in einem bevorzugten Zeichenformat zugreifen kann.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |msmapi32.dll  <br/> |
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
  
> [in] Das anfänglich entpackte Outlook-Objekt. Muss eine der folgenden Schnittstellen implementieren:
    
   - [IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx)oder [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).
    
_ulUnwrappedFlags_
  
> [in] Kennzeichen, die das nicht gepackte ursprüngliche Objekt kennzeichnen. Muss mindestens einer der folgenden Werte sein:
    
   - DDLWRAP_FLAG_ANSI: Das nicht gepackte Objekt ist ANSI.
    
   - DDLWRAP_FLAG_UNICODE: Das nicht gepackte Objekt ist UNICODE.
    
_ulWrappedFlags_
  
>  [in] Kennzeichen für das bevorzugte Zeichenformat. Muss mindestens einer der folgenden Werte sein: 
    
   - DDLWRAP_FLAG_ANSI: Das umschlossene Objekt wird als ANSI verfügbar gemacht.
    
   - DDLWRAP_FLAG_UNICODE: Das umschlossene Objekt wird als UNICODE verfügbar gemacht.
    
_pIID_
  
>  [in] Der Bezeichner der Schnittstelle, die vom nicht gepackten Objekt unterstützt wird; legen Sie ihn auf NULL fest, wenn dies unbekannt ist. 
    
_pulReserved_
  
>  [in] Dieser Parameter wird nicht verwendet. Er muss NULL sein. 
    
_fCheckWrap_
  
>  [in] Legen Sie diesen Parameter auf **"true"** fest, wenn  _"pvUnwrapped"_ vor dem Umbruch auf das Format überprüft werden soll. legen Sie ihn auf **"false"** fest, wenn das Objekt ohne Überprüfung umbrochen werden soll. 
    
_ppvWrapped_
  
>  [out] Ein Zeiger auf das angeforderte Objekt, umschlossen in das angeforderte Zeichenformat. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Übergeben eines umschlossenen Objekts, bei dem  _fCheckWrap_ auf **"true"** festgelegt ist, führt zu einem entpackten Objekt. Unabhängig davon, ob das zurückgegebene Objekt umbrochen wird, ist der Client für die Freigabe des Verweises auf das zurückgegebene Objekt verantwortlich. 
  
Wenn **Sie GetProcAddress** zum Suchen nach der Adresse dieser Funktion in msmapi32.dll verwenden, geben Sie **HrCreateNewWrappedObject@28** als Prozedurnamen an. 
  
## <a name="see-also"></a>Siehe auch

- [Über der Datenschicht Abbau API](about-the-data-degradation-layer-api.md)
- [Konstanten (Data Degradation Layer API)](constants-data-degradation-layer-api.md)

