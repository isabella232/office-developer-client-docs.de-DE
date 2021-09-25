---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Ruft einen vordefinierten Zeitraum für eine Aufzählung von Frei/Gebucht-Datenblöcken für einen Benutzer ab.
ms.openlocfilehash: 2480d781d5889515cbfe91c53a08a43436ed1d48
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614455"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

Ruft einen vordefinierten Zeitraum für eine Aufzählung von Frei/Gebucht-Datenblöcken für einen Benutzer ab.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a>Parameter

_prtmStart_
  
> [out] Ein relativer Zeitwert für den Beginn der Frei/Gebucht-Informationen. Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.
    
_prtmEnd_
  
> [out] Ein relativer Zeitwert für das Ende der Frei/Gebucht-Informationen. Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Bemerkungen

Ein Frei/Gebucht-Anbieter ruft [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) oder [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) auf, um den Zeitraum für eine Enumeration festzulegen. Wenn [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) oder [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) nicht aufgerufen wurde, müssen die Standardwerte für **prtmStart** und **prtmEnd** zwischen dem 1. April 1601 00:00:00Z und dem 31. August 4500 11:59:59Z festgelegt werden. Darüber hinaus sollten Sie nicht festlegen, dass die Startzeit größer als die Endzeit ist. 
  
**IFreeBusyData::GetFBPublishRange** muss die zwischengespeicherten Werte für den Zeitraum zurückgeben, der durch den letzten Aufruf von **IFreeBusyData::EnumBlocks** oder **IFreeBusyData::SetFBRange** festgelegt wurde. 
  
## <a name="see-also"></a>Siehe auch

- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

