---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Legt die Zeitspanne für eine Enumeration der Datenblöcke Frei/Gebucht-Informationen für einen Benutzer fest.
ms.openlocfilehash: 84a25a2dd43f594caa075d90e4f183086452184a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790978"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

Legt die Zeitspanne für eine Enumeration der Datenblöcke Frei/Gebucht-Informationen für einen Benutzer fest.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a>Parameter

_rtmStart_
  
> [in] Ein relative Zeitwert für den Anfang des Frei/Gebucht-Informationen. Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.
    
_rtmEnd_
  
> [in] Ein relative Zeitwert für das Ende des Frei/Gebucht-Informationen. Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Anmerkungen

Diese Methode wird verwendet, um den Zeitbereich des Kalenderelemente für das Abrufen von Details anzuzeigen. Die Werte der *FtmStart* und *FtmEnd* werden zwischengespeichert und in einem nachfolgenden Aufruf der [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)zurückgegeben.
  
## <a name="see-also"></a>Siehe auch

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [Verwenden Sie relative Zeit Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)

