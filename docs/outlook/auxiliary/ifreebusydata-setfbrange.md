---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Legt den Zeitraum für eine Aufzählung von Frei/Gebucht-Datenblöcken für einen Benutzer fest.
ms.openlocfilehash: 9e4c61eedf511dd9852cfe8e0c36cff525964815
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572214"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

Legt den Zeitraum für eine Aufzählung von Frei/Gebucht-Datenblöcken für einen Benutzer fest.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a>Parameter

_rtmStart_
  
> [in] Ein relativer Zeitwert für den Beginn der Frei/Gebucht-Informationen. Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.
    
_rtmEnd_
  
> [in] Ein relativer Zeitwert für das Ende der Frei/Gebucht-Informationen. Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Methode wird verwendet, um den Zeitraum von Kalenderelementen anzugeben, für die Details abgerufen werden sollen. Die Werte von  *ftmStart*  und  *ftmEnd*  werden zwischengespeichert und in einem nachfolgenden Aufruf von [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)zurückgegeben.
  
## <a name="see-also"></a>Siehe auch

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)

