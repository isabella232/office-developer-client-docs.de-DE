---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Ruft eine Schnittstelle ab, die Frei/Gebucht-Datenblöcke für einen Benutzer innerhalb eines angegebenen Zeitintervalls auflistet.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317556"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

Ruft eine Schnittstelle ab, die Frei/Gebucht-Datenblöcke für einen Benutzer innerhalb eines angegebenen Zeitintervalls auflistet.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Parameter

_ppenumfb_
  
> Out Eine Schnittstelle zum Auflisten von Frei/Gebucht-Blöcken.
    
_ftmStart_
  
> in Die Startzeit für die Enumeration. Sie wird in [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx)ausgedrückt.
    
_ftmEnd_
  
> in Die Endzeit für die Enumeration. Sie wird in **FILETIME**ausgedrückt. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Bemerkungen

Diese Methode wird verwendet, um den Zeitintervall der Kalenderelemente anzugeben, für die Details abgerufen werden sollen. Die Werte von *ftmStart* und *ftmEnd* werden zwischengespeichert und in einem nachfolgenden Aufruf von [IFreeBusyData:: GetFBPublishRange](ifreebusydata-getfbpublishrange.md)zurückgegeben.
  
Ein frei/gebucht-Anbieter kann auch anschließend die zurückgegebene [IEnumFBBlock](ienumfbblock.md) -Schnittstelle verwenden, um auf die Enumeration zuzugreifen. 
  
## <a name="see-also"></a>Siehe auch

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)

