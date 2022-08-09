<!-- get profile view -->
<div class="profile-view">
    <div class="profile-view-header">
        <div class="profile-view-header-left">
            <div class="profile-view-header-left-image">
                <img src="{{ $user->profile->avatar }}" alt="{{ $user->name }}">
            </div>
            <div class="profile-view-header-left-name">
                <h1>{{ $user->name }}</h1>
                <h2>{{ $user->profile->title }}</h2>
            </div>
        </div>
        <div class="profile-view-header-right">
            <div class="profile-view-header-right-follow">
                <a href="{{ route('follows.follow', $user->id) }}" class="btn btn-primary">Follow</a>
            </div>
            <div class="profile-view-header-right-followers">
                <p>{{ $user->followers()->count() }} followers</p>
            </div>
            <div class="profile-view-header-right-following">
                <p>{{ $user->following()->count() }} following</p>
            </div>
        </div>
    </div>
    <div class="profile-view-bio">
        <p>{{ $user->profile->bio }}</p>
    </div>
    <div class="profile-view-stats">
        <div class="profile-view-stats-item">
            <p>{{ $user->posts()->count() }}</p>
            <p>Posts</p>
        </div>
        <div class="profile-view-stats-item">
            <p>{{ $user->profile->followers()->count() }}</p>
            <p>Followers</p>
        </div>
        <div class="profile-view-stats-item">
            <p>{{ $user->following()->count() }}</p>
            <p>Following</p>
        </div>
    </div>
</div>