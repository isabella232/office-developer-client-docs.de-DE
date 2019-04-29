---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Legt den Zeitraum für eine Enumeration von Frei/Gebucht-Datenblöcken für einen Benutzer fest.
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421662"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

Legt den Zeitraum für eine Enumeration von Frei/Gebucht-Datenblöcken für einen Benutzer fest.
  
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
  
> in Ein relativer Zeitwert für den Beginn der Frei/Gebucht-Informationen. Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.
    
_rtmEnd_
  
> in Ein relativer Zeitwert für das Ende der Frei/Gebucht-Informationen. Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Bemerkungen

Diese Methode wird verwendet, um den Zeitintervall der Kalenderelemente anzugeben, für die Details abgerufen werden sollen. Die Werte von *ftmStart* und *ftmEnd* werden zwischengespeichert und in einem nachfolgenden Aufruf von [IFreeBusyData:: GetFBPublishRange](ifreebusydata-getfbpublishrange.md)zurückgegeben.
  
## <a name="see-also"></a>Siehe auch

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)

