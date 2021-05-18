---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Ruft eine Schnittstelle ab, die Frei/Gebucht-Datenblöcke für einen Benutzer innerhalb eines angegebenen Zeitbereichs aufzählt.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317556"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

Ruft eine Schnittstelle ab, die Frei/Gebucht-Datenblöcke für einen Benutzer innerhalb eines angegebenen Zeitbereichs aufzählt.
  
## <a name="quick-info"></a>QuickInfo

Weitere [Informationen finden Sie unter IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Parameter

_ppenumfb_
  
> [out] Eine Schnittstelle zum Aufzählen von Frei/Gebucht-Blöcken.
    
_ftmStart_
  
> [in] Die Startzeit für die Enumeration. Sie wird in [FILETIME ausgedrückt.](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx)
    
_ftmEnd_
  
> [in] Die Endzeit für die Enumeration. Sie wird in **FILETIME ausgedrückt.** 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Hinweise

Diese Methode wird verwendet, um den Zeitraum der Kalenderelemente anzugeben, für die Details abgerufen werden. Die Werte *von ftmStart* und *ftmEnd* werden zwischengespeichert und in einem nachfolgenden Aufruf von [IFreeBusyData::GetFBPublishRange zurückgegeben.](ifreebusydata-getfbpublishrange.md)
  
Ein Frei/Gebucht-Anbieter kann anschließend auch die zurückgegebene [IEnumFBBlock-Schnittstelle verwenden,](ienumfbblock.md) um auf die Enumeration zu zugreifen. 
  
## <a name="see-also"></a>Siehe auch

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)

