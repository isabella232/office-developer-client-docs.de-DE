---
title: Erstellen eines Termins, der ein ganztägiges Ereignis darstellt
TOCTitle: Create an appointment that is an all-day event
ms:assetid: a0d3baeb-6ed5-41b6-bef5-d6c1bb56fee3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184629(v=office.15)
ms:contentKeyID: 55119806
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5065395afe39247f8113bc5223b0e3e403a02fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349476"
---
# <a name="create-an-appointment-that-is-an-all-day-event"></a>Erstellen eines Termins, der ein ganztägiges Ereignis darstellt

In diesem Beispiel wird veranschaulicht, wie die [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\))-Eigenschaft verwendet wird, um einen Termin als ganztägiges Ereignis zu erstellen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Ein Ereignis unterscheidet sich insofern von einem normalen Termin, als es sich um eine Aktivität von mindestens 24-stündiger Dauer handelt. Beispiele für Ereignisse sind Messen, Seminare oder Urlaube. Ereignisse und jährliche Ereignisse werden nicht als belegte Zeiträume im Kalender des Benutzers angezeigt. Sie werden vielmehr als Banner dargestellt. Sie können die Banner am oberen Rand einer Tages- oder Wochenansicht des Kalenders sehen. Für einen ganztägigen Termin wird die Zeit des Benutzers anderen Personen gegenüber standardmäßig als gebucht angezeigt, für ein Ereignis oder jährliches Ereignis wird sie dagegen als frei angezeigt.

Um ein ganztägiges Ereignis programmgesteuert zu erstellen, legen Sie die [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\))-Eigenschaft des [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekts auf „true“ fest. Legen Sie dann die Eigenschaften [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) und [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) des AppointmentItem fest. Wenn Sie die AllDayEvent-Eigenschaft auf „true“ festlegen und die Start- und End-Eigenschaft nicht festlegen, findet das Ereignis heute statt, und es handelt sich um einen Termin, sodass der Status „Gebucht“ in Ihrem Kalender angezeigt wird. Sie müssen die Start- und End-Eigenschaft festlegen, wenn das Ereignis an einem Datum in der Zukunft stattfinden soll.

> [!NOTE]
> Um den Termin als ganztägiges Ereignis festzulegen, müssen Sie die Start-Eigenschaft auf 24:00 Uhr (Mitternacht) an dem Tag festlegen, an dem das Ereignis beginnen soll, und Sie müssen die End-Eigenschaft auf 24 Uhr an dem Tag festlegen, an dem das Ereignis enden soll. Wenn Sie die Start- oder Endzeit auf einen anderen Datums- oder Zeitwert als 24 Uhr festlegen, wird der Termin ein mehrtägiger Termin und kein ganztägiges Ereignis. 
>
> Wenn die Dauer beispielsweise nur ein Tag ist, legen Sie die Start-Eigenschaft auf 24 Uhr an dem Tag fest, an dem das Ereignis beginnen soll, und legen die End-Eigenschaft auf 24 Uhr am folgenden Tag fest. Sie sollten die End-Eigenschaft immer auf 12:00 Uhr an einem Datum festlegen, das einen Tag nach dem Startdatum liegt.

Im folgenden Codebeispiel wird von AllDayEventExample ein ganztägiges Ereignis erstellt, das am 11. Juni 2007 beginnt und am 15. Juni 2007 endet. Beachten Sie, dass die End-Eigenschaft für den Termin auf 00:00 Uhr am 16. Juni 2007 festgelegt wird.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AllDayEventExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Developer's Conference";
    appt.AllDayEvent = true;
    appt.Start = DateTime.Parse("6/11/2007 12:00 AM");
    appt.End = DateTime.Parse("6/16/2007 12:00 AM");
    appt.Display(false);
}
```

## <a name="see-also"></a>Siehe auch

- [Termine](appointments.md)

