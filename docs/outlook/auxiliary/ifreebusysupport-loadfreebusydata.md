---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Gibt für jeden angegebenen Benutzer eine Schnittstelle zum Auflisten von Frei/Gebucht-Datenblöcken innerhalb eines Zeitintervalls zurück.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411232"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Gibt für jeden angegebenen Benutzer eine Schnittstelle zum Auflisten von Frei/Gebucht-Datenblöcken innerhalb eines Zeitintervalls zurück. 
  
## <a name="quick-info"></a>QuickInfo

Siehe [IFreeBusySupport](ifreebusysupport.md).
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a>Parameter

_cMax_
  
> in Die Anzahl der [IFreeBusyData](ifreebusydata.md) -Schnittstellen, die zurückgegeben werden sollen. 
    
_rgfbuser_
  
> in Das Array der frei/gebucht-Benutzer, für das Daten abgerufen werden sollen.
    
_prgfbdata_
  
> in Out Das Array der **IFreeBusyData** -Schnittstellen, die dem _rgfbuser_ -Array von [FBUser](fbuser.md) -Strukturen entsprechen. 
    
   > [!NOTE]
   > Dieses Array von Zeigern wird vom Aufrufer zugewiesen und vom Aufrufer freigegeben. Die tatsächlichen Schnittstellen, auf die verwiesen wird, werden freigegeben, wenn der Aufrufer mit Ihnen ausgeführt wird. 
  
_phrStatus_
  
> Out Das Array der **HRESULT** -Ergebnisse zum Abrufen der jeweiligen **IFreeBusyData** -Schnittstelle. Der Wert kann NULL sein. Ein Ergebnis wird auf S_OK festgelegt, wenn die entsprechende _prgfbdata_ gültig ist. 
    
_pcRead_
  
>  Out Die tatsächliche Anzahl von Benutzern, für die eine **IFreeBusyData** -Schnittstelle gefunden wurde. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (frei/gebucht-API)](constants-free-busy-api.md)

