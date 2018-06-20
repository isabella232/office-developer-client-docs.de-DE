---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Dient zum Abrufen eines vordefinierten Zeitraums für eine Enumeration der Datenblöcke Frei/Gebucht-Informationen für einen Benutzer.
ms.openlocfilehash: 2a322a43da38a0b902789f4c83baaabd769154c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790960"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

Dient zum Abrufen eines vordefinierten Zeitraums für eine Enumeration der Datenblöcke Frei/Gebucht-Informationen für einen Benutzer.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a>Parameter

_prtmStart_
  
> [out] Ein relative Zeitwert für den Anfang des Frei/Gebucht-Informationen. Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.
    
_prtmEnd_
  
> [out] Ein relative Zeitwert für das Ende des Frei/Gebucht-Informationen. Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Anmerkungen

Ein Anbieter Frei/Gebucht-Informationen ruft [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) oder [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) , um den Zeitraum für eine Enumeration festzulegen. Wenn [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) oder [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) nicht aufgerufen wurde, müssen die Standardwerte für **PrtmStart** und **PrtmEnd** zwischen dem 1. April 1601 00:00:00Z und dem 31. August 4500 11:59:59Z festgelegt werden fest. Darüber hinaus sollten Sie die Startzeit größer sein als die Endzeit nicht festlegen. 
  
**IFreeBusyData::GetFBPublishRange** muss zurückgegeben werden, dass die zwischengespeicherten Werte für den Zeitraum vom letzten Aufruf für **IFreeBusyData::EnumBlocks** oder **IFreeBusyData::SetFBRange**festgelegt. 
  
## <a name="see-also"></a>Siehe auch

- [Verwenden Sie relative Zeit Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

