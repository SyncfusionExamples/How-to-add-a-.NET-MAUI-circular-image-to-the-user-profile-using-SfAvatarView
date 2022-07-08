# How-to-add-a-.NET-MAUI-circular-image-to-the-user-profile-using-SfAvatarView

The SfAvatarView provides a graphical representation of the user profile image that allows you to customize the view by adding a circle image, background color, icon, text, and more. The .NET MAUI circle image can be achieved using the SfAvatarView control with the avatar shape as a circle.

![.NET MAUI Circle Image User Profile](https://user-images.githubusercontent.com/97146406/177995298-a4ae0b4d-5822-42fc-812f-1534032c38c6.jpg)


## Steps to add .NET MAUI Circle Image

This section explains how to add a .NET MAUI circle image to the user profile using the SfAvatarView control. 

**Step 1:** Create a .NET MAUI application project in Visual Studio 2022.

**Step 2:** Add Syncfusion .NET MAUI [Avatar View](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.SfAvatarView.html?tabs=tabid-1) to your project, open the NuGet package manager in Visual Studio, search for [Syncfusion.Maui.Core](https://www.nuget.org/packages/Syncfusion.Maui.Core/) and then install it.

**Step 3:** In the **MauiProgram.cs** file, register the Syncfusion.Maui.Core handler as shown in the following code.

{% highlight C# hl_lines="1 12" %}

    using Syncfusion.Maui.Core.Hosting;

    namespace UserProfileSample;

    public static class MauiProgram
    {
        public static MauiApp CreateMauiApp()
        {
                var builder = MauiApp.CreateBuilder();
                builder
                    .UseMauiApp<App>()
                    .ConfigureSyncfusionCore()
                return builder.Build();
        }
    }

{% endhighlight %} 

**Step 4:** Add the Syncfusion.Maui.Core namespace to the MainPage.xaml.

{% highlight XAML %}

    xmlns:avatarview="clr-namespace:Syncfusion.Maui.Core;assembly=Syncfusion.Maui.Core"
	
{% endhighlight %}

**Step 5:** To add a .NET MAUI Circle Image in your .NET MAUI Application, define the SfAvatarView in the XAML and set the user image through the ImageSource property, set the AvatarShape property to the circle, render the profile image as a circle image, and add it to the user profile content page.

{% highlight C# %}
    <ContentPage.Content>
        <Grid HorizontalOptions="Center" VerticalOptions="Center" RowSpacing="30">

            <Grid.RowDefinitions>
                <RowDefinition Height="Auto"/>
                <RowDefinition Height="Auto"/>
            </Grid.RowDefinitions>

            <avatarview:SfAvatarView 
                            ContentType="Custom"
                            ImageSource="scarlett_jhonsan.png"
                            VerticalOptions="Center"
                            HorizontalOptions="Center"   
                            HeightRequest="100"
                            WidthRequest="100"
                            CornerRadius="50" />

            <Grid Grid.Row="1" ColumnSpacing="30" RowSpacing="15" >

                <Grid.RowDefinitions>
                    <RowDefinition Height="35"/>
                    <RowDefinition Height="35"/>
                    <RowDefinition Height="35"/>
                </Grid.RowDefinitions>

                <Grid.ColumnDefinitions>
                    <ColumnDefinition Width="25"/>
                    <ColumnDefinition Width="Auto"/>
                </Grid.ColumnDefinitions>


                <Image  Source="user.png" HeightRequest="25" VerticalOptions="Center"/>
                <Image Grid.Row="1" Source="call.png" HeightRequest="22" VerticalOptions="Center"/>
                <Image Grid.Row="2" Source="mail.png" HeightRequest="20"  VerticalOptions="Center" />

                <Label VerticalOptions="Start" Grid.Column="1" Text="Name" TextColor="Gray" FontSize="12"/>
                <Label VerticalOptions="End" Grid.Column="1" Text="Scarlett Jhonsan" FontAttributes="Bold"/>
                <Label VerticalOptions="Start"  Grid.Row="1" Grid.Column="1" Text="Phone" TextColor="Gray" FontSize="12"/>
                <Label VerticalOptions="End" Grid.Row="1" Grid.Column="1" Text="+44 5674 4432" FontAttributes="Bold"/>
                <Label VerticalOptions="Start" Grid.Row="2" Grid.Column="1" Text="Mail" TextColor="Gray" FontSize="12"/>
                <Label VerticalOptions="End" Grid.Row="2" Grid.Column="1" Text="scarlettjhonsan99@gmail.com" FontAttributes="Bold"/>

            </Grid>
        </Grid>
    </ContentPage.Content>
    
{% endhighlight %}


Note: Also, another way to add .NET MAUI Circle Image in your .NET MAUI Application, define the SfAvatarView in the XAML and set the user image through the ImageSource property, set the CornerRadius property to render the profile image as a circle image.

You can explore the runnable demo of adding the .NET MAUI circle Image on the above repository.


