---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Ruft einen vordefinierten Zeitraum für eine Enumeration von Frei/Gebucht-Datenblöcken für einen Benutzer ab.
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430077"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

Ruft einen vordefinierten Zeitraum für eine Enumeration von Frei/Gebucht-Datenblöcken für einen Benutzer ab.
  
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
  
> Out Ein relativer Zeitwert für den Beginn der Frei/Gebucht-Informationen. Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.
    
_prtmEnd_
  
> Out Ein relativer Zeitwert für das Ende der Frei/Gebucht-Informationen. Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Bemerkungen

Ein frei/gebucht-Anbieter ruft [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) oder [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) auf, um den Zeitintervall für eine Enumeration festzulegen. Wenn entweder [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) oder [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) nicht aufgerufen wurde, müssen die Standardwerte für **prtmStart** und **prtmEnd** zwischen dem 1. April 1601 00:00:00Z und dem 31. August 4500:59Z jeweils. Darüber hinaus sollten Sie die Startzeit nicht größer als die Endzeit festlegen. 
  
**IFreeBusyData:: GetFBPublishRange** muss die zwischengespeicherten Werte für den Zeitraum zurückgeben, der durch den letzten Aufruf für **IFreeBusyData:: EnumBlocks** oder **IFreeBusyData:: SetFBRange**festgelegt wurde. 
  
## <a name="see-also"></a>Siehe auch

- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

