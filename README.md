# sort-group-items-dynamically-listview-xamarin
How to sort the group items dynamically in  Xamarin.Forms ListView (SfListView)

## Sample

```xaml
<syncfusion:SfListView x:Name="listView" ItemSize="60" ItemsSource="{Binding ContactsInfo}" IsScrollBarVisible="False">
                <syncfusion:SfListView.ItemTemplate >
                    <DataTemplate>
                        <Grid x:Name="grid">
                            <Grid.ColumnDefinitions>
                                <ColumnDefinition Width="70" />
                                <ColumnDefinition Width="*" />
                                <ColumnDefinition Width="Auto" />
                            </Grid.ColumnDefinitions>
                            <Image Source="{Binding ContactImage}" VerticalOptions="Center" HorizontalOptions="Center" HeightRequest="50" WidthRequest="50"/>
                            <Grid Grid.Column="1" RowSpacing="1" Padding="10,0,0,0" VerticalOptions="Center">
                                <Label LineBreakMode="NoWrap" TextColor="#474747" Text="{Binding ContactName}"/>
                                <Label Grid.Row="1" Grid.Column="0" TextColor="#474747" LineBreakMode="NoWrap" Text="{Binding ContactNumber}"/>
                            </Grid>
                            <Label Text="{Binding ContactType}" FontSize="12" Grid.Column="2" Padding="0,0,10,0"/>
                        </Grid>
                    </DataTemplate>
                </syncfusion:SfListView.ItemTemplate>
                <syncfusion:SfListView.GroupHeaderTemplate>
                    <DataTemplate>
                                <StackLayout BackgroundColor="#E4E4E4">
                                    <Label Text="{Binding Key}"  FontSize="22" FontAttributes="Bold" VerticalOptions="Center" HorizontalOptions="Start" Margin="20,0,0,0" />
                                </StackLayout>
                    </DataTemplate>
                </syncfusion:SfListView.GroupHeaderTemplate>
            </syncfusion:SfListView>
```

## Requirements to run the demo

* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/) or [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/)
* Xamarin add-ons for Visual Studio (available via the Visual Studio installer).

## Troubleshooting

### Path too long exception

If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.
