---
title: IMAPIControl IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl
api_type:
- COM
ms.assetid: 5a647e15-ba22-4a7c-b235-75cd76b77c1a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8dce1415ef8d18f4b786e92324c888f9a0845162
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414039"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aktiviert und deaktiviert ein Schaltflächen-Steuerelement und führt Aufgaben aus, wenn ein Benutzer einer Clientanwendung auf das aktivierte Steuerelement klickt. Dienstanbieter implementieren Steuerelemente zum Erstellen benutzerdefinierter Schaltflächen in Dialogfeldern, wie beispielsweise Konfigurationseigenschaften Blätter, die mithilfe von Anzeige Tabellen definiert werden. 
  
Weitere Informationen zum Arbeiten mit Anzeige Tabellen und Steuerelementobjekten finden Sie unter [Display Tables](display-tables.md).
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Steuerelemente  <br/> |
|Implementiert von:  <br/> |Dienstanbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIControl  <br/> |
|Zeigertyp:  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterroraufzurufen](imapicontrol-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler der Schaltflächensteuerung enthält.  <br/> |
|[Activate](imapicontrol-activate.md) <br/> |Führt eine Aufgabe wie das Anzeigen eines Dialogfelds oder das Starten eines programmgesteuerten Vorgangs aus, wenn ein Benutzer der Clientanwendung auf das Schaltflächen-Steuerelement klickt.  <br/> |
|[GetState](imapicontrol-getstate.md) <br/> |Ruft einen Wert ab, der angibt, ob das Schaltflächen-Steuerelement aktiviert oder deaktiviert ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

