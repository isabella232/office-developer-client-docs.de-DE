---
title: Systematisches Freigeben von Objekten
TOCTitle: Systematically releasing objects
ms:assetid: d4cd1d8e-aae6-483b-a4d8-1656171e838d
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623945(v=office.15)
ms:contentKeyID: 55119785
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5d71ffbdbd10657832a319e1e669f38f311ad99f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708116"
---
# <a name="systematically-releasing-objects"></a>Systematisches Freigeben von Objekten

In diesem Thema finden Sie eine Zusammenfassung der Empfehlungen für das Herunterfahren von Add-Ins für Add-In-Entwickler und IT-Administratoren, die Outlook verwenden. Weitere Informationen finden Sie unter [Änderungen beim Herunterfahren für Outlook 2010](https://msdn.microsoft.com/library/ee720183\(v=office.15\)).

## <a name="add-in-shutdown-changes-in-outlook"></a>Änderungen beim Herunterfahren von Add-Ins in Outlook

Ab Outlook 2010 signalisiert Outlook standardmäßig nicht, dass Add-Ins heruntergefahren werden. Insbesondere ruft Outlook die **OnBeginShutdown(Array)**- und **OnDisconnection (ext\_DisconnectMode, Array)**-Methoden der **IDTExtensibility2**-Schnittstelle beim schnellen Herunterfahren nicht mehr auf. Ebenso ruft ein Outlook-Add-In, das mit Office-Entwicklungstools in Visual Studio 2010 oder höher geschrieben wurde, die ThisAddin\_Shutdown-Methode nicht mehr auf, wenn Outlook beendet wird. 

Der Grund dafür, dass diese Methoden nicht länger aufgerufen werden, liegt darin, dass während einige Add-Ins einfache Aufgaben wie das Freigeben von Referenzen während dieser Ereignisse durchführen, andere Add-Ins Webdienstaufrufe oder andere lange andauernde Vorgänge gleichzeitig ausführen, was zu erheblichen Verzögerungen beim Beenden von Outlook führte. Aufgrund dieser Änderung funktioniert Outlook nun besser als in der Vergangenheit beim Herunterfahren.

## <a name="recommendations-for-add-in-shutdown-for-developers"></a>Empfehlungen für das Herunterfahren von Add-Ins für Entwickler

Es ist wichtig, dass Entwickler sich an die folgenden Empfehlungen für das Herunterfahren von Add-Ins halten, damit die Endbenutzer weiterhin Outlook schnell herunterfahren können.

- Add-Ins sollten weiterhin die OnBeginShutdown- und die OnDisconnection-Methode oder ThisAddin\_Shutdown implementieren, um Verweise und reservierten Arbeitsspeicher freizugeben, weil Administratoren in bestimmten Szenarien vielleicht auf das langsame Herunterfahren über eine Gruppenrichtlinie zurückgreifen, oder weil der Benutzer das Add-In manuell über das Dialogfeld **COM-Add-Ins** trennen möchte.

- Add-In-Entwickler sollten nur Aufgaben ausführen, die unbedingt beim Herunterfahren erfolgen müssen.

- Add-In-Entwickler sollten die Leistung der Add-Ins in verschiedenen Szenarien und bei unterschiedlichen Windows-Registrierungseinstellungen zur Steuerung des Herunterfahrens von Outlook testen. Die Add-Ins sollten proaktiv für das Zusammenspiel mit Outlook angepasst werden.

## <a name="recommendations-for-add-in-shutdown-for-it-administrators"></a>Empfehlungen für das Herunterfahren von Add-Ins für IT-Administratoren

Wenn Add-Ins bereits in einem Unternehmen bereitgestellt sind und nicht geupgradet werden können, um Kompatibilität mit dem neuen Mechanismus zum Herunterfahren von Outlook herzustellen, können IT-Administratoren eine Reihe von Windows-Registrierungseinstellungen verwenden, um auf das langsame Herunterfahren umzusteigen.

### <a name="individual-add-in-setting"></a>Einstellung für ein einzelnes Add-In

IT-Administratoren können Benachrichtigungen für das Herunterfahren an einzelne Outlook-Add-Ins als Teil der Add-In-Bereitstellung aktivieren. Das ist zwar nicht über eine Gruppenrichtlinie möglich, doch empfiehlt es sich, Abwärtskompatibilität für bestimmte Add-Ins zu implementieren.

Konfigurieren Sie diese Einstellung für jedes Add-In über die Add-In-Registrierung in der HKCU- oder HKLM-Registrierungsstruktur, indem Sie der Add-In-Registrierung einen zusätzlichen Wert hinzufügen. Geben Sie den folgenden Text als eine einzige Zeile ein:

`HKCU\Software\Microsoft\Office\Outlook\Add-ins\<ProgID>[RequireShutdownNotification]=dword:0x1`

Wenn dieser Wert auf „0x1“ festgelegt wird, kann das Add-In blockierte Rückrufe beim Beenden von Outlook empfangen. Dies hat einen Einfluss auf die Leistung von Outlook beim Herunterfahren und sollte als Teil einer Bereitstellung erwogen werden. Diese Einstellung sollte nur, verwendet werden, wenn ein Add-In erhebliche Kompatibilitätsprobleme mit den neuen Mechanismen beim Herunterfahren aufweist. Wenn Sie den Wert auf 0x0 festlegen, wird das Standardverhalten von Outlook angewendet.

### <a name="global-setting"></a>Globale Einstellung

IT-Administratoren können Benachrichtigungen zum Herunterfahren global für alle Add-Ins mithilfe der Gruppenrichtlinie aktivieren. Dies empfiehlt sich für Organisationen mit einer großen Anzahl von internen Lösungen oder Desktops, für die diese Einstellung bereitgestellt werden muss, damit während eines Rollouts von Outlook die Kompatibilität gewährleistet ist.

Mit dieser Einstellung können Sie den Mechanismus für das Herunterfahren auf den von Outlook 2007 verwendeten umstellen. Sie können die Einstellung über die Gruppenrichtlinie entweder pro Benutzer oder pro Computer bereitstellen. Geben Sie den folgenden Text als einzelne Zeile ein:

`HKCU\Policies\Microsoft\Office\Outlook\15.0\Options\Shutdown[AddinFastShutdownBehavior]=dword:0x1`

Wenn Sie AddinFastShutdownBehavior auf „0x1“ festlegen, werden Benachrichtigungen für das Herunterfahren für alle Add-Ins aktiviert. Wenn Sie den Wert auf „0x0“ festlegen, wird das Standardverhalten von Outlook angewendet.

