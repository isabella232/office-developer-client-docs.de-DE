---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Ruft eine Schnittstelle ab, die Frei/Gebucht-Datenblöcke für einen Benutzer innerhalb eines angegebenen Zeitraums aufzählt.
ms.openlocfilehash: d33d4718707b44c481e5e54be47e4dad6b3b6bfa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572221"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

Ruft eine Schnittstelle ab, die Frei/Gebucht-Datenblöcke für einen Benutzer innerhalb eines angegebenen Zeitraums aufzählt.
  
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
  
> [out] Eine Schnittstelle zum Aufzählen von Frei/Gebucht-Blöcken.
    
_ftmStart_
  
> [in] Die Startzeit für die Enumeration. Er wird in [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx)ausgedrückt.
    
_ftmEnd_
  
> [in] Die Endzeit für die Enumeration. Er wird in **FILETIME** ausgedrückt. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Methode wird verwendet, um den Zeitraum von Kalenderelementen anzugeben, für die Details abgerufen werden sollen. Die Werte von  *ftmStart* und *ftmEnd* werden zwischengespeichert und in einem nachfolgenden Aufruf von [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)zurückgegeben.
  
Ein Frei/Gebucht-Anbieter kann anschließend auch die [zurückgegebene IEnumFBBlock-Schnittstelle](ienumfbblock.md) verwenden, um auf die Enumeration zuzugreifen. 
  
## <a name="see-also"></a>Siehe auch

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)

